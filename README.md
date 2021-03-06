# npmdoc-protobufjs

#### api documentation for  [protobufjs (v6.7.3)](http://dcode.io/protobuf.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-protobufjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-protobufjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-protobufjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-protobufjs)

#### Protocol Buffers for JavaScript (& TypeScript).

[![NPM](https://nodei.co/npm/protobufjs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/protobufjs)

- [https://npmdoc.github.io/node-npmdoc-protobufjs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-protobufjs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-protobufjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Wirtz"
    },
    "bin": {
        "pbjs": "bin/pbjs",
        "pbts": "bin/pbts"
    },
    "bugs": {
        "url": "https://github.com/dcodeIO/protobuf.js/issues"
    },
    "cliDependencies": [
        "semver",
        "chalk",
        "glob",
        "jsdoc",
        "minimist",
        "tmp",
        "uglify-js",
        "espree",
        "escodegen",
        "estraverse"
    ],
    "dependencies": {
        "@protobufjs/aspromise": "^1.1.1",
        "@protobufjs/base64": "^1.1.1",
        "@protobufjs/codegen": "^1.0.8",
        "@protobufjs/eventemitter": "^1.1.0",
        "@protobufjs/fetch": "^1.1.0",
        "@protobufjs/float": "^1.0.2",
        "@protobufjs/inquire": "^1.1.0",
        "@protobufjs/path": "^1.1.2",
        "@protobufjs/pool": "^1.1.0",
        "@protobufjs/utf8": "^1.1.0",
        "@types/long": "^3.0.31",
        "@types/node": "7.0.12",
        "long": "^3.2.0"
    },
    "description": "Protocol Buffers for JavaScript (& TypeScript).",
    "devDependencies": {
        "benchmark": "^2.1.4",
        "browserify": "^14.3.0",
        "browserify-wrap": "^1.0.2",
        "bundle-collapser": "^1.2.1",
        "chalk": "^1.1.3",
        "escodegen": "^1.8.1",
        "eslint": "^3.19.0",
        "espree": "^3.4.1",
        "estraverse": "^4.2.0",
        "gh-pages": "^0.12.0",
        "git-raw-commits": "^1.2.0",
        "git-semver-tags": "^1.2.0",
        "glob": "^7.1.1",
        "google-protobuf": "^3.2.0",
        "gulp": "^3.9.1",
        "gulp-header": "^1.8.8",
        "gulp-if": "^2.0.1",
        "gulp-sourcemaps": "^2.5.1",
        "gulp-uglify": "^2.1.2",
        "istanbul": "^0.4.5",
        "jaguarjs-jsdoc": "github:dcodeio/jaguarjs-jsdoc",
        "jsdoc": "^3.4.2",
        "minimist": "^1.2.0",
        "node-zopfli": "^2.0.2",
        "semver": "^5.3.0",
        "tap-spec": "^4.1.1",
        "tape": "^4.6.3",
        "tmp": "0.0.31",
        "tslint": "^5.0.0",
        "typescript": "^2.2.2",
        "uglify-js": "^2.8.21",
        "vinyl-buffer": "^1.0.0",
        "vinyl-fs": "^2.4.4",
        "vinyl-source-stream": "^1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9270aa5d75dfe4d37df1dec87c444a72140d0e1c",
        "tarball": "https://registry.npmjs.org/protobufjs/-/protobufjs-6.7.3.tgz"
    },
    "gitHead": "57f1da64945f2dc5537c6eaa53e08e8fdd477b67",
    "homepage": "http://dcode.io/protobuf.js",
    "keywords": [
        "protobuf",
        "protocol-buffers",
        "serialization",
        "typescript"
    ],
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "dcode"
        }
    ],
    "name": "protobufjs",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dcodeIO/protobuf.js.git"
    },
    "scripts": {
        "bench": "node bench",
        "build": "gulp --gulpfile scripts/gulpfile.js",
        "changelog": "node scripts/changelog -w",
        "coverage": "istanbul --config=config/istanbul.json cover node_modules/tape/bin/tape tests/*.js tests/node/*.js",
        "coverage-ci": "npm run coverage && codeclimate-test-reporter < coverage/lcov.info",
        "docs": "jsdoc -c config/jsdoc.json -R README.md --verbose --pedantic",
        "lint": "eslint **/*.js -c config/eslint.json && tslint **/*.d.ts -e **/node_modules/** -t stylish -c config/tslint.json",
        "make": "npm run test && npm run types && npm run build && npm run lint",
        "pages": "node scripts/pages",
        "postinstall": "node scripts/postinstall",
        "prepublish": "node scripts/prepublish",
        "prof": "node bench/prof",
        "release": "npm run make && npm run changelog",
        "test": "tape -r ./lib/tape-adapter tests/*.js tests/node/*.js | tap-spec",
        "test-types": "tsc tests/comp_typescript.ts --lib es2015 --noEmit --strictNullChecks && tsc tests/data/test.ts --lib es2015 --noEmit --strictNullChecks && tsc tests/data/rpc.ts --lib es2015 --noEmit --strictNullChecks",
        "types": "node bin/pbts --main --global protobuf --out index.d.ts src/ lib/aspromise/index.js lib/base64/index.js lib/codegen/index.js lib/eventemitter/index.js lib/float/index.js lib/fetch/index.js lib/inquire/index.js lib/path/index.js lib/pool/index.js lib/utf8/index.js && npm run test-types",
        "zuul": "zuul --ui tape --no-coverage --concurrency 4 -- tests/*.js",
        "zuul-local": "zuul --ui tape --concurrency 1 --local 8080 --disable-tunnel -- tests/*.js"
    },
    "types": "index.d.ts",
    "version": "6.7.3",
    "versionScheme": "~"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
