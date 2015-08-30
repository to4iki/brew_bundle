brew_bundle
===========

[![Build Status](https://travis-ci.org/to4iki/brew_bundle.svg)][status]
[![License][license-image]][license-url]

[status]: https://travis-ci.org/to4iki/brew_bundle

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

[MIT](http://to4iki.mit-license.org/)

## Author

[to4iki](https://github.com/to4iki)

[license-url]: http://to4iki.mit-license.org/
[license-image]: http://img.shields.io/badge/license-MIT-brightgreen.svg
