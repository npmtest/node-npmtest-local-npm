# npmtest-local-npm

#### test coverage for  [local-npm (v1.6.0)](https://github.com/nolanlawson/local-npm#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-local-npm.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-local-npm) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-local-npm.svg)](https://travis-ci.org/npmtest/node-npmtest-local-npm)

#### Local and offline-first npm mirror

[![NPM](https://nodei.co/npm/local-npm.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/local-npm)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-local-npm/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-local-npm/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-local-npm/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-local-npm/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-local-npm/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-local-npm/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-local-npm/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-local-npm/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-local-npm/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-local-npm/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-local-npm/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-local-npm/build/test-report.html](https://npmtest.github.io/node-npmtest-local-npm/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-local-npm/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-local-npm/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-local-npm/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-local-npm/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-local-npm/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-local-npm/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-local-npm/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-local-npm/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nolan Lawson"
    },
    "bin": {
        "local-npm": "lib/bin.js"
    },
    "bugs": {
        "url": "https://github.com/nolanlawson/local-npm/issues"
    },
    "dependencies": {
        "bluebird": "^2.2.2",
        "colors": "^0.6.2",
        "compression": "^1.0.10",
        "corser": "^2.0.0",
        "express": "^4.10.4",
        "express-http-proxy": "^0.6.0",
        "express-pouchdb": "^1.0.0",
        "level": "^1.3.0",
        "mkdirp": "^0.5.1",
        "morgan": "^1.2.2",
        "pouchdb": "^5.0.0",
        "request": "^2.39.0",
        "semver": "^5.0.1",
        "serve-favicon": "^2.0.1",
        "through2": "^2.0.0",
        "yargs": "^3.18.0"
    },
    "description": "Local and offline-first npm mirror",
    "devDependencies": {
        "babel-cli": "^6.4.0",
        "babel-eslint": "^4.1.6",
        "babel-plugin-syntax-async-functions": "^6.3.13",
        "babel-plugin-transform-regenerator": "^6.3.26",
        "babel-preset-es2015": "^6.3.13",
        "chai": "^3.4.1",
        "child-process-promise": "^1.1.0",
        "denodeify": "^1.2.1",
        "eslint": "^1.10.3",
        "istanbul": "^0.4.1",
        "istanbul-coveralls": "^1.0.3",
        "memdown": "^1.1.0",
        "mkdirp": "^0.5.1",
        "mocha": "^2.3.4",
        "ncp": "^2.0.0",
        "nock": "^5.2.1",
        "node-fetch": "^1.3.3",
        "rimraf": "^2.5.0",
        "run-scripts": "^0.4.0"
    },
    "directories": {},
    "dist": {
        "shasum": "53cdafb17b954e0ae6c810f1e3b5c7760441bf87",
        "tarball": "https://registry.npmjs.org/local-npm/-/local-npm-1.6.0.tgz"
    },
    "gitHead": "78c1487f9e36e46b189446c86399b6c472ed6106",
    "homepage": "https://github.com/nolanlawson/local-npm#readme",
    "license": "Apache-2.0",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "nolanlawson"
        },
        {
            "name": "cwmma"
        }
    ],
    "name": "local-npm",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/nolanlawson/local-npm.git"
    },
    "scripts": {
        "lint": "eslint lib/ test/",
        "main-test": "babel-node node_modules/.bin/_mocha --grep=$GREP test/test.js",
        "run-test": "run-scripts main-test test-cleanup",
        "start": "node ./lib/bin.js",
        "test": "echo \"There is no 'npm test'! Run ./test.sh instead.\" && exit 1",
        "test-cleanup": "rm -f .npmrc",
        "write-npmrc": "echo registry=http://127.0.0.1:3030/ > .npmrc"
    },
    "version": "1.6.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
