---
layout: post
title: How to build an (overly simplistic) housing data scraper
categories: [Python, Web-Scraping]
comments: true
---
In this article, I cover key information extraction (web scraping). The purpose of the article will be to extract key property information from the property site Trovit Homes ([https://homes.trovit.co.uk/](https://homes.trovit.co.uk/)).

The language used to demonstrate the steps in this article is python. However, there is very little difficulty required to port this code into whatever language you are using. 

### Embedded operations in the code

- making http requests to load raw html without running js on the target site
- parsing the raw html into an object that allows us to interact with the html and search it
- capability to search the html document by parsing it as xml and selecting tags based on their XPath
- storing attribute values for each of the selected tags in a csv for future use

# Recipe

### Determining the initial url to request

To determine the url pattern to pass into our script, first load the site in the browser and in this case carry out a property search in order to pull out the url pattern to use it in our script.

In this article, I will use *'Liverpool'* as the search term with the following filters set:

- for sale

This results in a url of the following form:

> [https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.**Liverpool**/isUserSearch.1](https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.Liverpool/isUserSearch.1)
> 

Further query parameters to pass into the url above can be determined by experimenting with the possible filter options for the search available on the site. (*These query parameters here actually appear as sub-paths for the above url-domain, but this is just how trovit have decided to manage their site and is purely stylistic*).

We might for example restrict the search to **Apartment**s which would correspond to:

> [https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.**Liverpool**/isUserSearch.1/property_type.Apartment](https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.Liverpool/isUserSearch.1/property_type.Apartment)
> 

### Paging

After the initial search, we notice that results are divided up into pages of 25 items at the time of writing. So it is also useful to investigate how the site's paging works so that we can obtain the full list of search results.

Manually viewing items from the second page in our browser, it is clear that paging is handled as an addition to the url path where the below represents results page 2:

> [https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.**Liverpool**/isUserSearch.1/property_type.Apartment**/page.2**](https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.Liverpool/isUserSearch.1/property_type.Apartment/page.2)
> 

### Extracting the page count

To extract the number of pages returned from our search, we must extract this information from the initial search page.

In this case, in the browser we can see the following part of the page:

![screen_capture for item count](/assets/images/screen_capture_simple_housing_scraper_item_count.jpeg){: .center }

which corresponds to the following html:

```html
<div class="results-counter js-results-counter"> 
	<p class="total_count"> 1-25 
		<strong>of 
			<span data-test="results">4,913</span> 
			properties for sale found
		</strong> 
	</p> 
</div>
```

We can use this to compute the number of pages by dividing the 4913 results count by the 25 items per page.

First, we add logic to the script to load the trovit site and perform the property search, this is exactly what we've done in the browser so far. The following logic makes the property search request:

```python
import bs4
import requests

search_term = 'Liverpool'
search_url = f'https://homes.trovit.co.uk/index.php/cod.search_homes/what_d.{search_term}/isUserSearch.1'
property_srch_url = f'{search_url}/origin.2/order_by.source_date/property_type.Apartment'
r    = requests.get(property_srch_url)
soup = bs4.BeautifulSoup(r.text,'html.parser')
```

In this step we:

1. request the page's html over http using the native python lib name requests
2. use a well-known python library to parse the html into a variable called soup

---

We then use the parsed html to extract the resulting item count and calculate a page count.

```python
total_item = soup.find('div', {'class':'results-counter js-results-counter'}).find('span').text
total_item = int(total_item.replace(',',''))
total_page = math.ceil(total_item/25)
```

I hard-code the 25 items into the code here because it is as domain specific as the selectors that I'm using to extract key information. Therefore the added complexity of parsing it from the page is out-weighed by the readability for this code snippet of explicitly writing 25.

### Parsing the page's html

Now that we have the number of pages stored as `total_page`,  we can extract key information from the results of each page.

I first request html for each page using the same logic as used in the step above:

```python
from lxml import etree # TODO: add this to the imports section of your script

while page <= total_page:
    property_srch_url_page = f'{property_srch_url}/page.{page}'
    r = requests.get(property_srch_url_page)
    soup_html = bs4.BeautifulSoup(r.text, 'html.parser')

    dom = etree.HTML(str(soup_html),parser=None)
```

Notice for this step, I additionally parse the requested html using a xml parser provided by the lxml package  by calling <span style="color: orange; font: 16px monospace;">etree.HTML(html_str)</span>. I do this so that I can use XPath selectors to select individual tags in the html.

<!-- <aside>
💡 *This xml parsing step simply allows us to query the html document as though it were xml.*

</aside> -->

<div class="callout">
  <div class="callout-icon-box">💡
  </div>
  <div class="callout-container">
    <p>This xml parsing step simply allows us to query the html document as though it were xml.</p>
  </div>
</div>

### Using XPath Selector to confirm the number of items on the page

The below statement locates a `div` tag in the html which has a class attribute equal to `"item-title"`. I query for all divs that match this selector because each result item contains a title like this. I then count the number of matches to determine the exact number of items on the page:

```python
nofitem = len(dom.xpath('//div[@class="item-title"]'))
```

## Extracting Key Information

I first define a couple of helper functions that contain logic to extract html tag contents. I do this to avoid needing to re-write this logic for each type of key information that we intend to extract. The helper functions simply wrap logic to:

1. Try to select a tag from the html based on the passed XPath selector
2. If such a tag exists, get the <span style="color: orange; font: 16px monospace;">i</span><sup>th</sup> match where <span style="color: orange; font: 16px monospace;">i</span> refers to the <span style="color: orange; font: 16px monospace;">i</span><sup>th</sup> result on the page that we want to extract information from

```python
def attr_from_xpath(xpath:str, num:int, attr_name:str='text'):
    try:
        item_xpath = xpath
        item = utils.xpath_attr_if_exists(dom, item_xpath, num, attr_name, defaultRes='')
        assert isinstance(item, str)
        item = item.replace(',','')
    except IndexError:
        item = "#NA"
    return item

def attr_from_item_xpath(item_name:str, num:int):
    return attr_from_xpath(xpath=f'//div[contains(@class,"item-{item_name}")]/span', num=num)
```

These functions are used to select tags containing key property information. For each match, I extract the attribute of interest and append the result to a list variable such as <span style="color: orange; font: 16px monospace;">title1</span> and <span style="color: orange; font: 16px monospace;">address1</span> below.

```python
while num < nofitem:            
    ## retrieving of the data
    
    app_logger.info(f'Retrieving titles for search page: {property_srch_url_page}')
    # Title
    title = attr_from_item_xpath('title', num)
    title1.append(title)
    
    # Address or Zone
    address = attr_from_item_xpath('address', num)
    address1.append(address)

		...
```

## Storage

In the interest of a quick and easy solution, we store the resulting lists in a python object (a pandas DataFrame). This object is provided by the well-known python library, pandas. If not familiar with this class, it can be thought of as a tabular data structure that can be queried and commanded in python.

<div class="callout">
  <div class="callout-icon-box">☝
  </div>
  <div class="callout-container">
    <p>We use the <i style="color: orange">DataFrame</i> for this article because data storage is outside of the scope of this tutorial and the api provided by the <i style="color: orange">pandas.DataFrame</i> class makes it easy to write the results to a csv file with only a few lines of code, (ideal for tutorials) 👍.</p>
  </div>
</div>

```python
dataframe = pd.DataFrame({
    'title': title1,
    'location': address1
})

dataframe.to_csv('results.csv',index=False)
```

# Conclusion

In this article, we have implemented a very basic web scraping script to pull property information from a well-known property search engine named Trovit Homes.

We have used a small number of python libraries to do this, but the actual steps performed can be carried out in any language as described above.

### Next Steps

In future development, we might look to make the script more robust with respect to the individual XPath selectors used to capture key information from the Trovit site. This would make the script more capable of being run on other property search engine domains and would make it more robust to future changes to the individual domain websites themselves.

---

Thanks for reading 😊