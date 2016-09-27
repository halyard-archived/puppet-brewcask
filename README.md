puppet-brewcask
===========

[![Puppet Forge](https://img.shields.io/puppetforge/v/halyard/brewcask.svg)](https://forge.puppetlabs.com/halyard/brewcask)
[![Dependency Status](https://img.shields.io/gemnasium/halyard/puppet-brewcask.svg)](https://gemnasium.com/halyard/puppet-brewcask)
[![MIT Licensed](http://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://tldrlegal.com/license/mit-license)
[![Build Status](https://img.shields.io/circleci/project/halyard/puppet-brewcask/master.svg)](https://circleci.com/gh/halyard/puppet-brewcask)

Module to tap [homebrew-cask](https://github.com/caskroom/homebrew-cask), and add `brewcask` provider for Puppet's package type.

## Changes from upstream

* Removed a lot of meta-stuff I wasn't using, like the cardboard scripts
* Set up CircleCI build tests

## Usage

```puppet
include brewcask # taps homebrew-cask / installs brew-cask

# now you can install packages using homebrew-cask
package { 'adium': provider => 'brewcask' }
package { 'firefox': provider => 'brewcask' }
```

## Required Puppet Modules

* [homebrew](https://github.com/halyard/puppet-homebrew)

