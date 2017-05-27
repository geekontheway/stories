source 'https://rubygems.org'
ruby "2.4.0"

gem 'rails', '4.2.8'
gem 'puma'
gem 'pg'

# Auth
gem 'devise'
gem 'omniauth-facebook'
gem 'omniauth-twitter'
gem 'omniauth-google-oauth2'

# Front-end
gem 'react-rails'
gem 'bootstrap-sass'
gem 'sass-rails'
gem 'font-awesome-sass'
gem 'uglifier'
gem 'autoprefixer-rails'

gem 'turbolinks'
gem 'jquery-rails'
gem 'jquery-ui-rails'
gem 'jbuilder'

gem 'friendly_id'

# Image upload
gem 'carrierwave'
gem 'mini_magick'
gem 'fog'
gem 'net-ssh'
gem 'sdoc', group: :doc

# Load will_paginate before elasticsearch gems.
gem 'will_paginate'

# Elasticsearch
gem 'elasticsearch-model'
gem 'elasticsearch-rails'

# Background Job
gem 'sidekiq'
gem 'sinatra', require: false
gem 'slim'
gem 'nokogiri'
# Caching
gem 'dalli'


# Use Capistrano for deployment
# gem 'capistrano-rails', group: :development

group :development, :test do
  gem 'byebug'
  gem 'rspec-rails'
  gem 'poltergeist'
  gem 'awesome_print'
  gem 'bundler-audit'
  gem 'pry-rails'
end

group :development do
  gem 'rails_best_practices'
  # Access an IRB console on exception pages or by using <%= console %> in views
  gem 'web-console'
  gem 'spring'
  gem 'guard-rspec', require: false
  gem 'spring-commands-rspec'
  gem 'rack-mini-profiler',  require: false
  gem 'annotate'
  gem 'bullet'
  gem 'quiet_assets'
end

group :test do
  gem 'database_cleaner'
  gem 'capybara'
  gem 'factory_girl_rails'
  gem 'faker'
  gem 'launchy'
  gem 'selenium-webdriver'
end

group :production do
  gem 'rails_12factor'
  gem 'bonsai-elasticsearch-rails'
end
