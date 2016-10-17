# oh-my-stack-templates

Opinionated Haskell project templates.

Create a library:

    stack new foobar https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-library.hsfiles

..with networking and file I/O:

    stack new foobar https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-network-service-library.hsfiles

## Synopsis

Templates for `stack new`, complementing the templates found in the [stack-templates](https://github.com/commercialhaskell/stack-templates) project.

## Features

* GHC 8 only
* Ready for some type level programming
* Heavily used dependencies added by default, including `singletons` and `lens`
* Unit tests based on `hspec`, `hspec-discover` and `QuickCheck`
* Benchmarks based on `criterion` 
* Travis-CI configuration
* `CHANGELOG.markdown`
* `README.markdown` with Hackage and Travis-CI batches
* A sane `.gitignore`
