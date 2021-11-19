Mocha Esbuild
=============

Run tests with mocha compiled by esbuild at lightning fast [soeeds](https://esbuild.github.io/). 

CLI requires a .esbuildrc.js file with an annotated example [here](https://github.com/RtVision/mocha-esbuild/blob/master/.esbuildrc.js)
while its possible it would work only the defaults it really depends on your projects setup.

I personally use this to compile vue SFC components then are tested with mocha and have seen pretty big speed increases.
One in partically that stood out to me was webpack building a single file took 1 minute and 15s while esbuild is it in about 15s.
When developing tests this time saving really adds up.


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/mocha-esbuild.svg)](https://npmjs.org/package/@rtvision/mocha-esbuild)
[![Downloads/week](https://img.shields.io/npm/dw/mocha-esbuild.svg)](https://npmjs.org/package/@rtvision/mocha-esbuild)
[![License](https://img.shields.io/npm/l/mocha-esbuild.svg)](https://github.com/RtVision/mocha-esbuild/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
<!-- tocstop -->
# Usage
```sh-session
mocha-esbuild --help
Run tests with mocha compiled by esbuild

USAGE
  $ mocha-esbuild [FILE]

ARGUMENTS
  FILE  [default: test/unit/**/*.spec.js] File path to the entry point to build from. Can be 1 specific file or take a globstar such as 'test/unit/**/*.spec.js'

OPTIONS
  -b, --bail                         Bail on the first test failure.
  -c, --color                        Color TTY output from reporter.
  -g, --grep=grep                    Test filter given regular expression.
  -h, --help                         show CLI help
  -p, --parallel                     Run test in parallel.
  -r, --require=require              Pathname of file that will be imported before tests run
  -s, --sourcemaps                   Generates inline sourcemaps for easier debugging. Will overwrite sourcemaps if custom config provided
  -t, --timeout=timeout              Timeout threshold value for mocha.
  -v, --version                      show CLI version
  -w, --watch                        Enable watch mode for esbuild. Will overwrite watch if custom config provided
  --esbuildConfig=esbuildConfig      [default: .esbuildrc.js] Esbuild config file path. The follow options will always be overwritten: bundle, stdin/entryPoints, and outfile
  --fgrep=fgrep                      Test filter given string
  --fullTrace=fullTrace              Full stacktrace upon failure?
  --invert                           Invert test filter matches?
  --jobs=jobs                        Max number of worker processes for parallel runs
  --mochaConfigPath=mochaConfigPath  Filepath to read mocha configs from, can be js or json file
  --reporter=reporter                Reporter name to use
  --retries=retries                  Number of times to retry failed tests
```
