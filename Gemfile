source "http://rubygems.org"

# Declare your gem's dependencies in blogit.gemspec.
# Bundler will treat runtime dependencies like base dependencies, and
# development dependencies will be added by default to the :development group.
gemspec

gem "rails", "~> 4.2.0"

# Removing this seems to break the Travis-CI flow.
# The rake task "app:acts_as_taggable_on_engine:install:migrations" doesn't work
# without it here
gem 'acts-as-taggable-on'

group :test do
  gem 'rake'
end
