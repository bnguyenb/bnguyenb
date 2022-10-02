---
layout: post
title:  How to install Bootstrap and jQuery in Rails 7 app with importmap
date:   2022-10-01 07:22:05 -0700
categories: development
path: "development"
tags: ["Ruby on Rails"]
---


#### First, add to your Gemfile
```ruby
gem 'jquery-rails'
gem 'bootstrap'
gem 'sassc-rails'
```
And run ```bundle install```

### Rename ```app/assets/stylesheets/application.css``` to ```app/assets/stylesheets/application.scss```

#### Then, add to ```application.scss``` above
```scss
@import "bootstrap";
```

#### Add to ```config/importmap.rb```
```ruby
pin "jquery", to: "jquery.min.js", preload: true
pin "jquery_ujs", to: "jquery_ujs.js", preload: true
pin "popper", to: "popper.js", preload: true
pin "bootstrap", to: "bootstrap.min.js", preload: true
```

#### Add to ```app/javascript/application.js```
```js
import "jquery"
import "jquery_ujs"
import "popper"
import "bootstrap"
```

#### This is all you need to have Bootstrap and jQuery fully working
