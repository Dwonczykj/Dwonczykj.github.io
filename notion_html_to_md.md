export the html from notion
set the layout to default_notion in the md header settings: layout: default_notion (this sets the style sheet)
remove the page properties table and header -> this is the header tag just after the tag
```html
<body><article id="43281ec4-c345-4ff8-8e9e-ca924a8fd710" class="page sans">
```

Wrap any Whimsical embed iframes in a responsive container div:
```html
<div class="responsive-iframe-container"><iframe class="responsive-iframe" style="border:none" src="https://whimsical.com/embed/TM67rPRGs5boowrueSZ2oN@2Ux7TurymMZ8y6zPcGwk"></iframe></div>
```