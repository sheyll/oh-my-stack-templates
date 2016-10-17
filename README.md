# oh-my-stack-templates

Collection of community Haskell project templates.

**Contributions are welcome! Please refer to: [contributing](CONTRIBUTING.markdown)**            

## Wait, what?

Templates for `stack new`, complementing the templates found in the [stack-templates](https://github.com/commercialhaskell/stack-templates) project.

The `stack-templates` project is currently searching a solution for modular, composable, upgradable, generic, safe stack templates.

Currently(10/2016) they are not too fond of PRs for new templates, until the general direction has been decided.

That's why this project was created. Until a correct solution has been found, I suggest we gather all our templates in here, 
and then kill this project as soon as `stack-templates` is done. 

I suggest it might make sense to gather many templates in order to deduce the requirements for a project like `stack-templates`.

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

### Build Commands and Flags

* Compile with `printf-debugging` enabled:
    
    stack build -f projectname:printfdebugging

* Run only light-weight tests:
    
    stack test -f projectname:-fulltests
   
* Run only light-weight benchmarks:
    
    stack test -f projectname:-fullbenchmarks


### Source Directories

    /src
        /library
        /tests
        /benchmarks

