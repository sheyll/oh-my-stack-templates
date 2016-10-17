# oh-my-stack-templates

Simple and stupid community Haskell project templates. (Just PR it)

## Synopsis

Templates for `stack new`, complementing the templates found in the [stack-templates](https://github.com/commercialhaskell/stack-templates) project.

## Usage

1. Pick a template from below and copy the URL of the template.
2. Change to the top-level directory where you keep your projects.
3. Define `author-email`, `author-name`, `github-username` and `copyright` in `~/.stack/config.yaml`
4. Run `stack new <projectname> <template-url> -p "category:<hackage-category>"`, e.g.:

    stack new skynet-core https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-library.hsfiles -p "category:machine-learning"

5. To override global settings, e.g. to use the organizations github user instead of your personal, supply corresponding `-p "key:value"` parameters, e.g.:

    stack new skynet-core https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-library.hsfiles -p "category:machine-learning" -p "github-username:cyberdyne"


# Available Templates 

## sheyll 

* [sheyll-library](https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-library.hsfiles)
* [sheyll-network-service-library](https://github.com/sheyll/oh-my-stack-templates/raw/master/sheyll-network-service-library.hsfiles)

### Source Directories

    /src
        /library
        /tests
        /benchmarks

### Features

#### `sheyll-library`

* GHC 8 only
* Many syntax extension
* Many type level programming extensions and dependencies
* `bytestring`, `vector`, `binary`, `lens`, `text`, `array`, `pretty`, `parsec`, `exceptions`, `mtl`, `containers`, `singletons`, `uuid` and other _pure-ish_ dependencies
* _IO-ish_ dependencies: `random`, `time`
* Unit tests based on `hspec`, `hspec-discover` and `QuickCheck`
* Benchmarks based on `criterion` 
* Travis-CI configuration
* `CHANGELOG.markdown`
* `README.markdown` with Hackage and Travis-CI batches
* A sane `.gitignore`

#### `sheyll-network-service-library`

* Super-set of `sheyll-library`
* Additional _IO-ish_ dependencies: `resource`, `process`, `random`, `async`, `stm`, `network`, `streaming-commons`
