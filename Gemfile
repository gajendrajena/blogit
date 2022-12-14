source "http://rubygems.org"

# Declare your gem's dependencies in blogit.gemspec.
# Bundler will treat runtime dependencies like base dependencies, and
# development dependencies will be added by default to the :development group.
gemspec

rails_version = ENV["RAILS_VERSION"] || "default"

rails_v = case rails_version
when "master"
  { github: "rails/rails" }
when "default"
  "~> 6.1.6"
else
  "~> #{rails_version}"
end

gem "rails", rails_v

# If we're using Rails 3 - include the
# strong_parameters gem. Otherwise, it should be inluded as part of Rails 4
if rails_version[0] == '3'
  gem 'strong_parameters'
end

gem 'rake', '>= 12.2'

# Removing this seems to break the Travis-CI flow.
# The rake task "app:acts_as_taggable_on_engine:install:migrations" doesn't work
# without it here
gem 'acts-as-taggable-on', "~> 9.0.1"
