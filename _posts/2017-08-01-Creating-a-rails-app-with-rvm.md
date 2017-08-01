---
layout: post
title:  "Creating a Ruby on Rails app with RVM on Ubuntu"
date:   2017-08-01 08:17:00 +0000
categories: ruby-on-rails
---

I wrote this step-by-step to help me remember it next time I create an app.

It's my first time experimenting with Rails. I wanted to use a virtual environment from the start because that's how I learned Python-Django too, and to not be afraid of setting things up.

This guide might grow as I learn more details of the process. For example, at this point I'm not sure how updates to the system Ruby version would affect the project.

I'm using Ubuntu 16.10.

### Install Ruby
### Install rvm

### Create virtual environment
```
$ rvm gemset create <name>
```

### Activate virtual environment
```
$ rvm @<name>
```

### Check which one is being used
```
$ rvm gemset list

gemsets for ruby-2.4.0 (found in /home/felipe/.rvm/gems/ruby-2.4.0)
   (default)
   global
=> learn_rails
```

### Install rails
```
$ gem install rails
```

## Check rails
```
$ rails --version

Rails 5.1.X
```

### Create new app
```
$ rails new blog
$ cd blog
```

### Run server
```
$ bin/rails server
```

###### I got an error:
```
@learn_rails/gems/bundler-1.15.3/lib/bundler/runtime.rb:85:in `rescue in block (2 levels) in require': There was an error while trying to load the gem 'uglifier'. (Bundler::GemRequireError)
```

A JS runtime was missing. So I went to blog/Gemfile and uncommented line 20:
```ruby
gem 'therubyracer', platforms: :ruby/
```

Then installed the new gem.
```
$ bundle install
Bundle complete! 17 Gemfile dependencies, 73 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```

Now the server ran fine:
```
$ bin/rails server
```

Browse to: http://localhost:3000

All set!
