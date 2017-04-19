# npmtest-zxcvbn

#### basic test coverage for  [zxcvbn (v4.4.2)](https://github.com/dropbox/zxcvbn#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-zxcvbn.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-zxcvbn) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-zxcvbn.svg)](https://travis-ci.org/npmtest/node-npmtest-zxcvbn)

#### realistic password strength estimation

[![NPM](https://nodei.co/npm/zxcvbn.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/zxcvbn)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-zxcvbn/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-zxcvbn/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-zxcvbn/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-zxcvbn/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-zxcvbn/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-zxcvbn/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-zxcvbn/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-zxcvbn/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-zxcvbn/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-zxcvbn/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-zxcvbn/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-zxcvbn/build/test-report.html](https://npmtest.github.io/node-npmtest-zxcvbn/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-zxcvbn/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-zxcvbn/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-zxcvbn/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-zxcvbn/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-zxcvbn/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-zxcvbn/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-zxcvbn/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-zxcvbn/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Wheeler"
    },
    "bugs": {
        "url": "https://github.com/dropbox/zxcvbn/issues"
    },
    "dependencies": {},
    "description": "realistic password strength estimation",
    "devDependencies": {
        "browserify": "^11.0.1",
        "coffee-coverage": "^0.6.3",
        "coffee-script": "^1.10.0",
        "coffeeify": "^1.1.0",
        "coffeetape": "^1.0.1",
        "exorcist": "^0.4.0",
        "faucet": "^0.0.1",
        "istanbul": "^0.3.18",
        "tape": "^4.2.0",
        "uglifyify": "^3.0.1",
        "watchify": "^3.3.1",
        "zuul": "^3.4.0"
    },
    "directories": {},
    "dist": {
        "shasum": "28ec17cf09743edcab056ddd8b1b06262cc73c30",
        "tarball": "https://registry.npmjs.org/zxcvbn/-/zxcvbn-4.4.2.tgz"
    },
    "gitHead": "f0735425180b130d6c57efbc044a47c0c8f1fd65",
    "homepage": "https://github.com/dropbox/zxcvbn#readme",
    "keywords": [
        "password",
        "passphrase",
        "security",
        "authentication",
        "strength",
        "meter",
        "quality",
        "estimation",
        "pattern",
        "cracking",
        "scoring",
        "entropy",
        "bruteforce"
    ],
    "license": "MIT",
    "main": "lib/main.js",
    "maintainers": [
        {
            "name": "wheels"
        }
    ],
    "name": "zxcvbn",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dropbox/zxcvbn.git"
    },
    "scripts": {
        "build": "npm run build-lib ; npm run build-dist",
        "build-dist": "browserify --debug  --standalone zxcvbn -t coffeeify --extension='.coffee' -t uglifyify src/main.coffee |   exorcist --base . dist/zxcvbn.js.map >| dist/zxcvbn.js",
        "build-lib": "coffee -o lib --compile --bare --map src/*.coffee",
        "prepublish": "npm run build",
        "test": "coffeetape test/*.coffee | faucet",
        "test-saucelabs": "zuul -- test/*.coffee",
        "watch": "npm run watch-lib & npm run watch-dist",
        "watch-dist": "watchify --debug -v --standalone zxcvbn -t coffeeify --extension='.coffee' -t uglifyify src/main.coffee -o 'exorcist --base . dist/zxcvbn.js.map >| dist/zxcvbn.js'",
        "watch-lib": "coffee -o lib --compile --bare --map --watch src/*.coffee"
    },
    "version": "4.4.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
