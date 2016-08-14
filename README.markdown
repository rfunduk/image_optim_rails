[![Gem Version](https://img.shields.io/gem/v/image_optim_rails.svg?style=flat)](https://rubygems.org/gems/image_optim_rails)
[![Build Status](https://img.shields.io/travis/toy/image_optim_rails/master.svg?style=flat)](https://travis-ci.org/toy/image_optim_rails)
[![Code Climate](https://img.shields.io/codeclimate/github/toy/image_optim_rails.svg?style=flat)](https://codeclimate.com/github/toy/image_optim_rails)
[![Dependency Status](https://img.shields.io/gemnasium/toy/image_optim_rails.svg?style=flat)](https://gemnasium.com/toy/image_optim_rails)
[![Inch CI](https://inch-ci.org/github/toy/image_optim_rails.svg?branch=master&style=flat)](https://inch-ci.org/github/toy/image_optim_rails)

# image\_optim\_rails

Optimize rails image assets using image_optim gem.

Options and instructions for getting binaries can be found in [image_optim readme](https://github.com/toy/image_optim).

## Installation

Add to your `Gemfile`:

```ruby
gem 'image_optim'
```

With [`image_optim_pack`](https://github.com/toy/image_optim_pack):

```ruby
gem 'image_optim'
gem 'image_optim_pack'
```

## Usage

`ImageOptim::Railtie` will automatically register sprockets preprocessor unless you set `config.assets.image_optim = false` or `config.assets.compress = false` (later for partial rails 3 compatibility).

You can provide options for image_optim used for preprocessor through config:

```ruby
config.assets.image_optim.nice = 20
config.assets.image_optim.svgo = false
```

Check available options in [options section of image_optim](https://github.com/toy/image_optim#options).

Image optimization can be time consuming, so depending on your deployment process you may prefer to optimize original asset files.

## Copyright

Copyright (c) 2013-2016 Ivan Kuchin. See [LICENSE.txt](LICENSE.txt) for details.
