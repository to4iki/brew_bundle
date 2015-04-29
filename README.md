brew_bundle
===========

[![Build Status](https://travis-ci.org/to4iki/brew_bundle.svg)][status]
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)][license]

[status]: https://travis-ci.org/to4iki/brew_bundle
[license]: https://github.com/to4iki/brew_bundle/master/LICENSE

Homebrew package & application install.

## Description

use [itamae-kitchen/itamae](https://github.com/itamae-kitchen/itamae)

## Usage

### Installation

```bash
$ gem i bundler
```

```bash
$ git clone git@github.com:to4iki/brew_bundle.git
$ bundle install --path vendor/bundle
```

### Execute

```bash
$ bundle exec rake brew:bundle
```

##### Dryrun

```bash
$ bundle exec rake brew:dryrun
```

### Spec

```bash
$ bundle exec rake spec
```

## Licence

[MIT](https://github.com/to4iki/brew_bundle/master/LICENSE)

## Author

[to4iki](https://github.com/to4iki)
