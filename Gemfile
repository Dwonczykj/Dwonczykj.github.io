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