# Setting up the blog on Github.io

[GitHub Pages](https://pages.github.com/)

We begin by installing ruby:

```ruby
which ruby
which gem
```

if ruby or rubygem is not installed:

```ruby
brew install ruby
```

We next install Jekyll, (the static site bundler that will give us templating and dynamic markdown for our github blog:

```ruby
# Install Jekyll and Bundler:
gem install jekyll bundler
```

We then get jekyll to give us a starting template to configure in our local git repo:

cd to the git repo and then call:

```ruby
jekyll new .
```

We then need to open the gemfile and change it to be configured as below inline with the current dependency graph so that all the gems can be installed using `bundle update`

Compatible versions of the are inline with the depencencies in the below bookmark and configured as so:

[https://pages.github.com/versions/](https://pages.github.com/versions/)

```ruby
source "https://rubygems.org"

# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
gem "jekyll", "~> 3.9.0"

# To update to the latest github dependencies run: `bundle update`
# To list current versions: `bundle exec github-pages versions`
# Check github versions: https://pages.github.com/versions/
gem "github-pages", "~> 225", group: :jekyll_plugins

group :jekyll_plugins do
  gem 'jekyll-feed', "~> 0.15.1"
  gem 'jekyll-paginate', "~> 1.1.0"
  gem 'jekyll-seo-tag', "~> 2.8.0"
  gem 'jekyll-sitemap', "~> 1.4.0"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :install_if => Gem.win_platform?
```

### [localhost:4000](http://localhost:4000) check point

run the below command to check that the bundle is servable locally and can be accessed at localhost:4000

```ruby
bundle exec jekyll serve --drafts --livereload
```

For those running Windows, I recommend adding `--force_polling`. Otherwise, saving your content sometimes does not auto-regenerate the site.

The code for this currently sits under the _site folder in your repo.

---

Now we start to configure the site and add some templates to style our blog posts.

## Style sheets

The layout of the style sheets is to have a main style sheet named site.scss. This style sheet imports the rest of the style sheets in the _sass folder. The _sass folder is known by jekyll (_config.yml) to be the location of the style sheets. We can change the folder name in the config using:
```YAML
# sass:
#   sass_dir: _sass
```
Then finally, there is a linking file located in assets/css/style.scss which imports the site.scss and exposes the styles defined there to the public site.