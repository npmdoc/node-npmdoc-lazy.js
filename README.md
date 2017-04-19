# npmdoc-lazy.js

#### api documentation for  [lazy.js (v0.5.0)](http://dtao.github.io/lazy.js/)  [![npm package](https://img.shields.io/npm/v/npmdoc-lazy.js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-lazy.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-lazy.js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-lazy.js)

#### Like Underscore, but lazier

[![NPM](https://nodei.co/npm/lazy.js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/lazy.js)

- [https://npmdoc.github.io/node-npmdoc-lazy.js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-lazy.js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-lazy.js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Tao",
        "url": "http://philosopherdeveloper.com"
    },
    "browser": "lazy.js",
    "bugs": {
        "url": "https://github.com/dtao/lazy.js/issues"
    },
    "dependencies": {},
    "description": "Like Underscore, but lazier",
    "devDependencies": {
        "JSONStream": "0.10.0",
        "autodoc": "0.6.4",
        "benchmark": "1.0.0",
        "deft": "0.2.2",
        "jasmine-async": "0.0.1",
        "jasmine-node": "1.13.x",
        "jsdoc": "3.2.x",
        "lodash": "4.2.1",
        "memorystream": "0.2.0",
        "promises-aplus-tests": "2.1.0",
        "race.js": "0.1.4",
        "requirejs": "^2.1.20",
        "string-table": "0.1.2",
        "underscore": "1.8.3"
    },
    "directories": {},
    "dist": {
        "shasum": "d8a02be135806fcbbcd7999513d8b6faf9857550",
        "tarball": "https://registry.npmjs.org/lazy.js/-/lazy.js-0.5.0.tgz"
    },
    "gitHead": "b69fb65cf2b67087b4e8e4c8c8f619fb94306b42",
    "homepage": "http://dtao.github.io/lazy.js/",
    "keywords": [
        "lazy",
        "functional",
        "performance",
        "speed",
        "util"
    ],
    "license": "MIT",
    "main": "lazy.node.js",
    "maintainers": [
        {
            "name": "dtao"
        }
    ],
    "name": "lazy.js",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dtao/lazy.js.git"
    },
    "scripts": {
        "amd": "node spec/amd_spec.js",
        "autodoc": "autodoc -t --variable Lazy lazy.js",
        "jasmine": "jasmine-node spec/node_spec.js",
        "promise": "promises-aplus-tests spec/async_handle_adapter --reporter dot --bail",
        "test": "npm run-script 'autodoc' && npm run-script 'jasmine' && npm run-script 'amd' && npm run-script 'promise'"
    },
    "version": "0.5.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
