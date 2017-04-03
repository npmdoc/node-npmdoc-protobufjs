# api documentation for  [protobufjs (v6.7.0)](http://dcode.io/protobuf.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-protobufjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-protobufjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-protobufjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-protobufjs)
#### Protocol Buffers for JavaScript (& TypeScript).

[![NPM](https://nodei.co/npm/protobufjs.png?downloads=true)](https://www.npmjs.com/package/protobufjs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-protobufjs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-protobufjs/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-protobufjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Wirtz",
        "email": "dcode+protobufjs@dcode.io"
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
        "browserify": "^14.1.0",
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
        "gulp": "^3.9.1",
        "gulp-header": "^1.8.8",
        "gulp-if": "^2.0.1",
        "gulp-sourcemaps": "^2.5.0",
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
        "shasum": "ba201ab60b26755c53b044f5f7f000bb2dc0cf2b",
        "tarball": "https://registry.npmjs.org/protobufjs/-/protobufjs-6.7.0.tgz"
    },
    "gitHead": "7a0b5b1cab22df03d9627ffe3b17cf6014f9a0fc",
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
            "name": "dcode",
            "email": "dcode@dcode.io"
        }
    ],
    "name": "protobufjs",
    "optionalDependencies": {
        "@types/long": "^3.0.31",
        "@types/node": "7.0.12",
        "long": "^3.2.0"
    },
    "readme": "ERROR: No README data found!",
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
    "version": "6.7.0",
    "versionScheme": "~"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module protobufjs](#apidoc.module.protobufjs)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>BufferReader (buffer)](#apidoc.element.protobufjs.BufferReader)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>BufferWriter ()](#apidoc.element.protobufjs.BufferWriter)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Class (type, ctor)](#apidoc.element.protobufjs.Class)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Enum (name, values, options)](#apidoc.element.protobufjs.Enum)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Field (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>MapField (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Message (properties)](#apidoc.element.protobufjs.Message)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Method (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Namespace (name, options)](#apidoc.element.protobufjs.Namespace)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>OneOf (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Reader (buffer)](#apidoc.element.protobufjs.Reader)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>ReflectionObject (name, options)](#apidoc.element.protobufjs.ReflectionObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Root (options)](#apidoc.element.protobufjs.Root)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Service (name, options)](#apidoc.element.protobufjs.Service)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Type (name, options)](#apidoc.element.protobufjs.Type)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Writer ()](#apidoc.element.protobufjs.Writer)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>common (name, json)](#apidoc.element.protobufjs.common)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>configure ()](#apidoc.element.protobufjs.configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>decoder (mtype)](#apidoc.element.protobufjs.decoder)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>encoder (mtype)](#apidoc.element.protobufjs.encoder)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>load (filename, root, callback)](#apidoc.element.protobufjs.load)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>loadSync (filename, root)](#apidoc.element.protobufjs.loadSync)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>parse (source, root, options)](#apidoc.element.protobufjs.parse)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>rpc.Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>tokenize (source)](#apidoc.element.protobufjs.tokenize)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.codegen ()](#apidoc.element.protobufjs.util.codegen)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>util.float (exports)](#apidoc.element.protobufjs.util.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>verifier (mtype)](#apidoc.element.protobufjs.verifier)
1.  object <span class="apidocSignatureSpan">protobufjs.</span>BufferReader.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>BufferWriter.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Enum.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Field.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>MapField.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Message.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Method.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Namespace.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>OneOf.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Reader.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>ReflectionObject.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Root.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Service.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Type.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>Writer.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>converter
1.  object <span class="apidocSignatureSpan">protobufjs.</span>debug
1.  object <span class="apidocSignatureSpan">protobufjs.</span>roots
1.  object <span class="apidocSignatureSpan">protobufjs.</span>rpc
1.  object <span class="apidocSignatureSpan">protobufjs.</span>rpc.Service.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>types
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.Buffer.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.EventEmitter.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.Long.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.LongBits.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.ProtocolError.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.base64
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.path
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.toJSONOptions
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.toJSONOptions.longs.prototype
1.  object <span class="apidocSignatureSpan">protobufjs.</span>util.utf8
1.  string <span class="apidocSignatureSpan">protobufjs.</span>build

#### [module protobufjs.BufferReader](#apidoc.module.protobufjs.BufferReader)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>BufferReader (buffer)](#apidoc.element.protobufjs.BufferReader.BufferReader)

#### [module protobufjs.BufferReader.prototype](#apidoc.module.protobufjs.BufferReader.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>_slice (start, end)](#apidoc.element.protobufjs.BufferReader.prototype._slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>constructor (buffer)](#apidoc.element.protobufjs.BufferReader.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>string ()](#apidoc.element.protobufjs.BufferReader.prototype.string)

#### [module protobufjs.BufferWriter](#apidoc.module.protobufjs.BufferWriter)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>BufferWriter ()](#apidoc.element.protobufjs.BufferWriter.BufferWriter)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferWriter.</span>alloc (size)](#apidoc.element.protobufjs.BufferWriter.alloc)

#### [module protobufjs.BufferWriter.prototype](#apidoc.module.protobufjs.BufferWriter.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>bytes (value)](#apidoc.element.protobufjs.BufferWriter.prototype.bytes)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>constructor ()](#apidoc.element.protobufjs.BufferWriter.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>string (value)](#apidoc.element.protobufjs.BufferWriter.prototype.string)

#### [module protobufjs.Class](#apidoc.module.protobufjs.Class)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Class (type, ctor)](#apidoc.element.protobufjs.Class.Class)
1.  [function <span class="apidocSignatureSpan">protobufjs.Class.</span>create (type, ctor)](#apidoc.element.protobufjs.Class.create)
1.  [function <span class="apidocSignatureSpan">protobufjs.Class.</span>generate (type)](#apidoc.element.protobufjs.Class.generate)

#### [module protobufjs.Enum](#apidoc.module.protobufjs.Enum)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Enum (name, values, options)](#apidoc.element.protobufjs.Enum.Enum)
1.  [function <span class="apidocSignatureSpan">protobufjs.Enum.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Enum.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Enum.</span>className

#### [module protobufjs.Enum.prototype](#apidoc.module.protobufjs.Enum.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>add (name, id, comment)](#apidoc.element.protobufjs.Enum.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>constructor (name, values, options)](#apidoc.element.protobufjs.Enum.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>remove (name)](#apidoc.element.protobufjs.Enum.prototype.remove)
1.  [function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Enum.prototype.toJSON)

#### [module protobufjs.Field](#apidoc.module.protobufjs.Field)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Field (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field.Field)
1.  [function <span class="apidocSignatureSpan">protobufjs.Field.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Field.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Field.</span>className

#### [module protobufjs.Field.prototype](#apidoc.module.protobufjs.Field.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>constructor (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>resolve ()](#apidoc.element.protobufjs.Field.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>setOption (name, value, ifNotSet)](#apidoc.element.protobufjs.Field.prototype.setOption)
1.  [function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Field.prototype.toJSON)

#### [module protobufjs.MapField](#apidoc.module.protobufjs.MapField)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>MapField (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField.MapField)
1.  [function <span class="apidocSignatureSpan">protobufjs.MapField.</span>fromJSON (name, json)](#apidoc.element.protobufjs.MapField.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.MapField.</span>className

#### [module protobufjs.MapField.prototype](#apidoc.module.protobufjs.MapField.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>constructor (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>resolve ()](#apidoc.element.protobufjs.MapField.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>toJSON ()](#apidoc.element.protobufjs.MapField.prototype.toJSON)

#### [module protobufjs.Message](#apidoc.module.protobufjs.Message)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Message (properties)](#apidoc.element.protobufjs.Message.Message)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>decode (reader)](#apidoc.element.protobufjs.Message.decode)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>decodeDelimited (reader)](#apidoc.element.protobufjs.Message.decodeDelimited)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>encode (message, writer)](#apidoc.element.protobufjs.Message.encode)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>encodeDelimited (message, writer)](#apidoc.element.protobufjs.Message.encodeDelimited)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>from (object)](#apidoc.element.protobufjs.Message.from)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>fromObject (object)](#apidoc.element.protobufjs.Message.fromObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>toObject (message, options)](#apidoc.element.protobufjs.Message.toObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.</span>verify (message)](#apidoc.element.protobufjs.Message.verify)

#### [module protobufjs.Message.prototype](#apidoc.module.protobufjs.Message.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Message.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.Message.prototype.</span>toObject (options)](#apidoc.element.protobufjs.Message.prototype.toObject)

#### [module protobufjs.Method](#apidoc.module.protobufjs.Method)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Method (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method.Method)
1.  [function <span class="apidocSignatureSpan">protobufjs.Method.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Method.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Method.</span>className

#### [module protobufjs.Method.prototype](#apidoc.module.protobufjs.Method.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>constructor (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>resolve ()](#apidoc.element.protobufjs.Method.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Method.prototype.toJSON)

#### [module protobufjs.Namespace](#apidoc.module.protobufjs.Namespace)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Namespace (name, options)](#apidoc.element.protobufjs.Namespace.Namespace)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>_configure (Type_, Service_)](#apidoc.element.protobufjs.Namespace._configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>arrayToJSON (array)](#apidoc.element.protobufjs.Namespace.arrayToJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Namespace.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Namespace.</span>className

#### [module protobufjs.Namespace.prototype](#apidoc.module.protobufjs.Namespace.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>add (object)](#apidoc.element.protobufjs.Namespace.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>addJSON (nestedJson)](#apidoc.element.protobufjs.Namespace.prototype.addJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Namespace.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>define (path, json)](#apidoc.element.protobufjs.Namespace.prototype.define)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>get (name)](#apidoc.element.protobufjs.Namespace.prototype.get)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>getEnum (name)](#apidoc.element.protobufjs.Namespace.prototype.getEnum)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookup (path, filterTypes, parentAlreadyChecked)](#apidoc.element.protobufjs.Namespace.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupEnum (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupEnum)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupService (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupService)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupType (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupType)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupTypeOrEnum (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupTypeOrEnum)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>remove (object)](#apidoc.element.protobufjs.Namespace.prototype.remove)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Namespace.prototype.resolveAll)
1.  [function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Namespace.prototype.toJSON)

#### [module protobufjs.OneOf](#apidoc.module.protobufjs.OneOf)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>OneOf (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf.OneOf)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.</span>fromJSON (name, json)](#apidoc.element.protobufjs.OneOf.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.OneOf.</span>className

#### [module protobufjs.OneOf.prototype](#apidoc.module.protobufjs.OneOf.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>add (field)](#apidoc.element.protobufjs.OneOf.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>constructor (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>onAdd (parent)](#apidoc.element.protobufjs.OneOf.prototype.onAdd)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>onRemove (parent)](#apidoc.element.protobufjs.OneOf.prototype.onRemove)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>remove (field)](#apidoc.element.protobufjs.OneOf.prototype.remove)
1.  [function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>toJSON ()](#apidoc.element.protobufjs.OneOf.prototype.toJSON)

#### [module protobufjs.Reader](#apidoc.module.protobufjs.Reader)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Reader (buffer)](#apidoc.element.protobufjs.Reader.Reader)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.</span>_configure (BufferReader_)](#apidoc.element.protobufjs.Reader._configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.</span>create (buffer)](#apidoc.element.protobufjs.Reader.create)

#### [module protobufjs.Reader.prototype](#apidoc.module.protobufjs.Reader.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>_slice ()](#apidoc.element.protobufjs.Reader.prototype._slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>bool ()](#apidoc.element.protobufjs.Reader.prototype.bool)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>bytes ()](#apidoc.element.protobufjs.Reader.prototype.bytes)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>double ()](#apidoc.element.protobufjs.Reader.prototype.double)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>fixed32 ()](#apidoc.element.protobufjs.Reader.prototype.fixed32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>fixed64 ()](#apidoc.element.protobufjs.Reader.prototype.fixed64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>float ()](#apidoc.element.protobufjs.Reader.prototype.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>int32 ()](#apidoc.element.protobufjs.Reader.prototype.int32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>int64 ()](#apidoc.element.protobufjs.Reader.prototype.int64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sfixed32 ()](#apidoc.element.protobufjs.Reader.prototype.sfixed32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sfixed64 ()](#apidoc.element.protobufjs.Reader.prototype.sfixed64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sint32 ()](#apidoc.element.protobufjs.Reader.prototype.sint32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sint64 ()](#apidoc.element.protobufjs.Reader.prototype.sint64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>skip (length)](#apidoc.element.protobufjs.Reader.prototype.skip)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>skipType (wireType)](#apidoc.element.protobufjs.Reader.prototype.skipType)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>string ()](#apidoc.element.protobufjs.Reader.prototype.string)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>uint32 ()](#apidoc.element.protobufjs.Reader.prototype.uint32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>uint64 ()](#apidoc.element.protobufjs.Reader.prototype.uint64)

#### [module protobufjs.ReflectionObject](#apidoc.module.protobufjs.ReflectionObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>ReflectionObject (name, options)](#apidoc.element.protobufjs.ReflectionObject.ReflectionObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.</span>_configure (Root_)](#apidoc.element.protobufjs.ReflectionObject._configure)
1.  string <span class="apidocSignatureSpan">protobufjs.ReflectionObject.</span>className

#### [module protobufjs.ReflectionObject.prototype](#apidoc.module.protobufjs.ReflectionObject.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>getOption (name)](#apidoc.element.protobufjs.ReflectionObject.prototype.getOption)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>onAdd (parent)](#apidoc.element.protobufjs.ReflectionObject.prototype.onAdd)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>onRemove (parent)](#apidoc.element.protobufjs.ReflectionObject.prototype.onRemove)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>resolve ()](#apidoc.element.protobufjs.ReflectionObject.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>setOption (name, value, ifNotSet)](#apidoc.element.protobufjs.ReflectionObject.prototype.setOption)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>setOptions (options, ifNotSet)](#apidoc.element.protobufjs.ReflectionObject.prototype.setOptions)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>toJSON ()](#apidoc.element.protobufjs.ReflectionObject.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>toString ()](#apidoc.element.protobufjs.ReflectionObject.prototype.toString)

#### [module protobufjs.Root](#apidoc.module.protobufjs.Root)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Root (options)](#apidoc.element.protobufjs.Root.Root)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.</span>_configure (Type_, parse_, common_)](#apidoc.element.protobufjs.Root._configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.</span>fromJSON (json, root)](#apidoc.element.protobufjs.Root.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Root.</span>className

#### [module protobufjs.Root.prototype](#apidoc.module.protobufjs.Root.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>_handleAdd (object)](#apidoc.element.protobufjs.Root.prototype._handleAdd)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>_handleRemove (object)](#apidoc.element.protobufjs.Root.prototype._handleRemove)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>constructor (options)](#apidoc.element.protobufjs.Root.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>load (filename, options, callback)](#apidoc.element.protobufjs.Root.prototype.load)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>loadSync (filename, options)](#apidoc.element.protobufjs.Root.prototype.loadSync)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Root.prototype.resolveAll)
1.  [function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>resolvePath (originPath, includePath, alreadyNormalized)](#apidoc.element.protobufjs.Root.prototype.resolvePath)

#### [module protobufjs.Service](#apidoc.module.protobufjs.Service)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Service (name, options)](#apidoc.element.protobufjs.Service.Service)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Service.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Service.</span>className

#### [module protobufjs.Service.prototype](#apidoc.module.protobufjs.Service.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>add (object)](#apidoc.element.protobufjs.Service.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Service.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>create (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.Service.prototype.create)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>get (name)](#apidoc.element.protobufjs.Service.prototype.get)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>remove (object)](#apidoc.element.protobufjs.Service.prototype.remove)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Service.prototype.resolveAll)
1.  [function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Service.prototype.toJSON)

#### [module protobufjs.Type](#apidoc.module.protobufjs.Type)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Type (name, options)](#apidoc.element.protobufjs.Type.Type)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Type.fromJSON)
1.  string <span class="apidocSignatureSpan">protobufjs.Type.</span>className

#### [module protobufjs.Type.prototype](#apidoc.module.protobufjs.Type.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>add (object)](#apidoc.element.protobufjs.Type.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Type.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>create (properties)](#apidoc.element.protobufjs.Type.prototype.create)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>decode (reader, length)](#apidoc.element.protobufjs.Type.prototype.decode)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>decodeDelimited (reader)](#apidoc.element.protobufjs.Type.prototype.decodeDelimited)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>encode (message, writer)](#apidoc.element.protobufjs.Type.prototype.encode)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>encodeDelimited (message, writer)](#apidoc.element.protobufjs.Type.prototype.encodeDelimited)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>from (object)](#apidoc.element.protobufjs.Type.prototype.from)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>fromObject (object)](#apidoc.element.protobufjs.Type.prototype.fromObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>get (name)](#apidoc.element.protobufjs.Type.prototype.get)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>isReservedId (id)](#apidoc.element.protobufjs.Type.prototype.isReservedId)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>isReservedName (name)](#apidoc.element.protobufjs.Type.prototype.isReservedName)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>remove (object)](#apidoc.element.protobufjs.Type.prototype.remove)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Type.prototype.resolveAll)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>setup ()](#apidoc.element.protobufjs.Type.prototype.setup)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Type.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>toObject (message, options)](#apidoc.element.protobufjs.Type.prototype.toObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>verify (message)](#apidoc.element.protobufjs.Type.prototype.verify)

#### [module protobufjs.Writer](#apidoc.module.protobufjs.Writer)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>Writer ()](#apidoc.element.protobufjs.Writer.Writer)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.</span>_configure (BufferWriter_)](#apidoc.element.protobufjs.Writer._configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.</span>alloc (size)](#apidoc.element.protobufjs.Writer.alloc)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.</span>create ()](#apidoc.element.protobufjs.Writer.create)

#### [module protobufjs.Writer.prototype](#apidoc.module.protobufjs.Writer.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>bool (value)](#apidoc.element.protobufjs.Writer.prototype.bool)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>bytes (value)](#apidoc.element.protobufjs.Writer.prototype.bytes)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>double (value)](#apidoc.element.protobufjs.Writer.prototype.double)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>finish ()](#apidoc.element.protobufjs.Writer.prototype.finish)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fixed32 (value)](#apidoc.element.protobufjs.Writer.prototype.fixed32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fixed64 (value)](#apidoc.element.protobufjs.Writer.prototype.fixed64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>float (value)](#apidoc.element.protobufjs.Writer.prototype.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fork ()](#apidoc.element.protobufjs.Writer.prototype.fork)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>int32 (value)](#apidoc.element.protobufjs.Writer.prototype.int32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>int64 (value)](#apidoc.element.protobufjs.Writer.prototype.int64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>ldelim ()](#apidoc.element.protobufjs.Writer.prototype.ldelim)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>push (fn, len, val)](#apidoc.element.protobufjs.Writer.prototype.push)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>reset ()](#apidoc.element.protobufjs.Writer.prototype.reset)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sfixed32 (value)](#apidoc.element.protobufjs.Writer.prototype.sfixed32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sfixed64 (value)](#apidoc.element.protobufjs.Writer.prototype.sfixed64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sint32 (value)](#apidoc.element.protobufjs.Writer.prototype.sint32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sint64 (value)](#apidoc.element.protobufjs.Writer.prototype.sint64)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>string (value)](#apidoc.element.protobufjs.Writer.prototype.string)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>uint32 (value)](#apidoc.element.protobufjs.Writer.prototype.uint32)
1.  [function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>uint64 (value)](#apidoc.element.protobufjs.Writer.prototype.uint64)

#### [module protobufjs.converter](#apidoc.module.protobufjs.converter)
1.  [function <span class="apidocSignatureSpan">protobufjs.converter.</span>fromObject (mtype)](#apidoc.element.protobufjs.converter.fromObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.converter.</span>toObject (mtype)](#apidoc.element.protobufjs.converter.toObject)

#### [module protobufjs.debug](#apidoc.module.protobufjs.debug)
1.  [function <span class="apidocSignatureSpan">protobufjs.debug.</span>disable ()](#apidoc.element.protobufjs.debug.disable)
1.  [function <span class="apidocSignatureSpan">protobufjs.debug.</span>enable ()](#apidoc.element.protobufjs.debug.enable)
1.  [function <span class="apidocSignatureSpan">protobufjs.debug.</span>unusedTypes (ns)](#apidoc.element.protobufjs.debug.unusedTypes)

#### [module protobufjs.rpc](#apidoc.module.protobufjs.rpc)
1.  [function <span class="apidocSignatureSpan">protobufjs.rpc.</span>Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service)

#### [module protobufjs.rpc.Service](#apidoc.module.protobufjs.rpc.Service)
1.  [function <span class="apidocSignatureSpan">protobufjs.rpc.</span>Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service.Service)

#### [module protobufjs.rpc.Service.prototype](#apidoc.module.protobufjs.rpc.Service.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>constructor (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>end (endedByRPC)](#apidoc.element.protobufjs.rpc.Service.prototype.end)
1.  [function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>rpcCall (method, requestCtor, responseCtor, request, callback)](#apidoc.element.protobufjs.rpc.Service.prototype.rpcCall)

#### [module protobufjs.tokenize](#apidoc.module.protobufjs.tokenize)
1.  [function <span class="apidocSignatureSpan">protobufjs.</span>tokenize (source)](#apidoc.element.protobufjs.tokenize.tokenize)
1.  [function <span class="apidocSignatureSpan">protobufjs.tokenize.</span>unescape (str)](#apidoc.element.protobufjs.tokenize.unescape)

#### [module protobufjs.util](#apidoc.module.protobufjs.util)
1.  boolean <span class="apidocSignatureSpan">protobufjs.util.</span>isNode
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>Array ()](#apidoc.element.protobufjs.util.Array)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>_Buffer_allocUnsafe (size)](#apidoc.element.protobufjs.util._Buffer_allocUnsafe)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>_Buffer_from (value, encodingOrOffset, length)](#apidoc.element.protobufjs.util._Buffer_from)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>_configure ()](#apidoc.element.protobufjs.util._configure)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>asPromise (fn, ctx)](#apidoc.element.protobufjs.util.asPromise)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>codegen ()](#apidoc.element.protobufjs.util.codegen)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>compareFieldsById (a, b)](#apidoc.element.protobufjs.util.compareFieldsById)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>float (exports)](#apidoc.element.protobufjs.util.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>inquire (moduleName)](#apidoc.element.protobufjs.util.inquire)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>isInteger ()](#apidoc.element.protobufjs.util.isInteger)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>isObject (value)](#apidoc.element.protobufjs.util.isObject)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>isSet (obj, prop)](#apidoc.element.protobufjs.util.isSet)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>isString (value)](#apidoc.element.protobufjs.util.isString)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>isset (obj, prop)](#apidoc.element.protobufjs.util.isset)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>lazyResolve (root, lazyTypes)](#apidoc.element.protobufjs.util.lazyResolve)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>lcFirst (str)](#apidoc.element.protobufjs.util.lcFirst)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>longFromHash (hash, unsigned)](#apidoc.element.protobufjs.util.longFromHash)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>longToHash (value)](#apidoc.element.protobufjs.util.longToHash)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>merge (dst, src, ifNotSet)](#apidoc.element.protobufjs.util.merge)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>newBuffer (sizeOrArray)](#apidoc.element.protobufjs.util.newBuffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>newError (name)](#apidoc.element.protobufjs.util.newError)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>oneOfGetter (fieldNames)](#apidoc.element.protobufjs.util.oneOfGetter)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>oneOfSetter (fieldNames)](#apidoc.element.protobufjs.util.oneOfSetter)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>pool (alloc, slice, size)](#apidoc.element.protobufjs.util.pool)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>safeProp (name)](#apidoc.element.protobufjs.util.safeProp)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>toArray (object)](#apidoc.element.protobufjs.util.toArray)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>ucFirst (str)](#apidoc.element.protobufjs.util.ucFirst)
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>base64
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>emptyArray
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>emptyObject
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>key2Re
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>key32Re
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>key64Re
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>path
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>toJSONOptions
1.  object <span class="apidocSignatureSpan">protobufjs.util.</span>utf8

#### [module protobufjs.util.Buffer](#apidoc.module.protobufjs.util.Buffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer.Buffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>alloc (size, fill, encoding)](#apidoc.element.protobufjs.util.Buffer.alloc)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>allocUnsafe (size)](#apidoc.element.protobufjs.util.Buffer.allocUnsafe)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>allocUnsafeSlow (size)](#apidoc.element.protobufjs.util.Buffer.allocUnsafeSlow)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>byteLength (string, encoding)](#apidoc.element.protobufjs.util.Buffer.byteLength)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>compare (a, b)](#apidoc.element.protobufjs.util.Buffer.compare)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>concat (list, length)](#apidoc.element.protobufjs.util.Buffer.concat)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>from (value, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer.from)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>isBuffer (b)](#apidoc.element.protobufjs.util.Buffer.isBuffer)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>isEncoding (encoding)](#apidoc.element.protobufjs.util.Buffer.isEncoding)
1.  number <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>poolSize

#### [module protobufjs.util.Buffer.prototype](#apidoc.module.protobufjs.util.Buffer.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>asciiSlice ()](#apidoc.element.protobufjs.util.Buffer.prototype.asciiSlice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>asciiWrite ()](#apidoc.element.protobufjs.util.Buffer.prototype.asciiWrite)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>base64Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.base64Slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>base64Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.base64Write)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.protobufjs.util.Buffer.prototype.compare)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>copy ()](#apidoc.element.protobufjs.util.Buffer.prototype.copy)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>equals (b)](#apidoc.element.protobufjs.util.Buffer.prototype.equals)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.fill)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>hexSlice ()](#apidoc.element.protobufjs.util.Buffer.prototype.hexSlice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>hexWrite ()](#apidoc.element.protobufjs.util.Buffer.prototype.hexWrite)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.includes)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>inspect ()](#apidoc.element.protobufjs.util.Buffer.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>latin1Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.latin1Slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>latin1Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.latin1Write)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readDoubleBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readDoubleLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readFloatBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readFloatLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt16BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt16LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt32BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt32LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt8)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readIntBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readIntLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt16BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt16LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt32BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt32LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt8)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUIntBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUIntLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>slice (start, end)](#apidoc.element.protobufjs.util.Buffer.prototype.slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap16 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap16)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap32 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap32)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap64 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap64)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>toJSON ()](#apidoc.element.protobufjs.util.Buffer.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>toString ()](#apidoc.element.protobufjs.util.Buffer.prototype.toString)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>ucs2Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.ucs2Slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>ucs2Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.ucs2Write)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>utf8Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.utf8Slice)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>utf8Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.utf8Write)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.write)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeFloatBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeFloatLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt16BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt16LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt32BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt32LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt8)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeIntBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeIntLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32BE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32LE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt8)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUIntBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUIntLE)

#### [module protobufjs.util.EventEmitter](#apidoc.module.protobufjs.util.EventEmitter)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter.EventEmitter)

#### [module protobufjs.util.EventEmitter.prototype](#apidoc.module.protobufjs.util.EventEmitter.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>emit (evt)](#apidoc.element.protobufjs.util.EventEmitter.prototype.emit)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>off (evt, fn)](#apidoc.element.protobufjs.util.EventEmitter.prototype.off)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>on (evt, fn, ctx)](#apidoc.element.protobufjs.util.EventEmitter.prototype.on)

#### [module protobufjs.util.Long](#apidoc.module.protobufjs.util.Long)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long.Long)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromBits (lowBits, highBits, unsigned)](#apidoc.element.protobufjs.util.Long.fromBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromInt (value, unsigned)](#apidoc.element.protobufjs.util.Long.fromInt)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromNumber (value, unsigned)](#apidoc.element.protobufjs.util.Long.fromNumber)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromString (str, unsigned, radix)](#apidoc.element.protobufjs.util.Long.fromString)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromValue (val)](#apidoc.element.protobufjs.util.Long.fromValue)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>isLong (obj)](#apidoc.element.protobufjs.util.Long.isLong)
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>MAX_UNSIGNED_VALUE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>MAX_VALUE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>MIN_VALUE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>NEG_ONE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>ONE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>UONE
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>UZERO
1.  object <span class="apidocSignatureSpan">protobufjs.util.Long.</span>ZERO

#### [module protobufjs.util.Long.prototype](#apidoc.module.protobufjs.util.Long.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>add (addend)](#apidoc.element.protobufjs.util.Long.prototype.add)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>and (other)](#apidoc.element.protobufjs.util.Long.prototype.and)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>comp (other)](#apidoc.element.protobufjs.util.Long.prototype.comp)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>compare (other)](#apidoc.element.protobufjs.util.Long.prototype.compare)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>div (divisor)](#apidoc.element.protobufjs.util.Long.prototype.div)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>divide (divisor)](#apidoc.element.protobufjs.util.Long.prototype.divide)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>eq (other)](#apidoc.element.protobufjs.util.Long.prototype.eq)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>equals (other)](#apidoc.element.protobufjs.util.Long.prototype.equals)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getHighBits ()](#apidoc.element.protobufjs.util.Long.prototype.getHighBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getHighBitsUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.getHighBitsUnsigned)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getLowBits ()](#apidoc.element.protobufjs.util.Long.prototype.getLowBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.getLowBitsUnsigned)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getNumBitsAbs ()](#apidoc.element.protobufjs.util.Long.prototype.getNumBitsAbs)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>greaterThan (other)](#apidoc.element.protobufjs.util.Long.prototype.greaterThan)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.protobufjs.util.Long.prototype.greaterThanOrEqual)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>gt (other)](#apidoc.element.protobufjs.util.Long.prototype.gt)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>gte (other)](#apidoc.element.protobufjs.util.Long.prototype.gte)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isEven ()](#apidoc.element.protobufjs.util.Long.prototype.isEven)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isNegative ()](#apidoc.element.protobufjs.util.Long.prototype.isNegative)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isOdd ()](#apidoc.element.protobufjs.util.Long.prototype.isOdd)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isPositive ()](#apidoc.element.protobufjs.util.Long.prototype.isPositive)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isZero ()](#apidoc.element.protobufjs.util.Long.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lessThan (other)](#apidoc.element.protobufjs.util.Long.prototype.lessThan)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lessThanOrEqual (other)](#apidoc.element.protobufjs.util.Long.prototype.lessThanOrEqual)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lt (other)](#apidoc.element.protobufjs.util.Long.prototype.lt)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lte (other)](#apidoc.element.protobufjs.util.Long.prototype.lte)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>mod (divisor)](#apidoc.element.protobufjs.util.Long.prototype.mod)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>modulo (divisor)](#apidoc.element.protobufjs.util.Long.prototype.modulo)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>mul (multiplier)](#apidoc.element.protobufjs.util.Long.prototype.mul)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>multiply (multiplier)](#apidoc.element.protobufjs.util.Long.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>neg ()](#apidoc.element.protobufjs.util.Long.prototype.neg)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>negate ()](#apidoc.element.protobufjs.util.Long.prototype.negate)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>neq (other)](#apidoc.element.protobufjs.util.Long.prototype.neq)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>not ()](#apidoc.element.protobufjs.util.Long.prototype.not)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>notEquals (other)](#apidoc.element.protobufjs.util.Long.prototype.notEquals)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>or (other)](#apidoc.element.protobufjs.util.Long.prototype.or)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftLeft (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftLeft)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftRight (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftRight)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftRightUnsigned)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shl (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shl)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shr (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shr)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shru (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shru)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>sub (subtrahend)](#apidoc.element.protobufjs.util.Long.prototype.sub)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>subtract (subtrahend)](#apidoc.element.protobufjs.util.Long.prototype.subtract)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytes (le)](#apidoc.element.protobufjs.util.Long.prototype.toBytes)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytesBE ()](#apidoc.element.protobufjs.util.Long.prototype.toBytesBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytesLE ()](#apidoc.element.protobufjs.util.Long.prototype.toBytesLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toInt ()](#apidoc.element.protobufjs.util.Long.prototype.toInt)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toNumber ()](#apidoc.element.protobufjs.util.Long.prototype.toNumber)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toSigned ()](#apidoc.element.protobufjs.util.Long.prototype.toSigned)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toString (radix)](#apidoc.element.protobufjs.util.Long.prototype.toString)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.toUnsigned)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>xor (other)](#apidoc.element.protobufjs.util.Long.prototype.xor)

#### [module protobufjs.util.LongBits](#apidoc.module.protobufjs.util.LongBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits.LongBits)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>from (value)](#apidoc.element.protobufjs.util.LongBits.from)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>fromHash (hash)](#apidoc.element.protobufjs.util.LongBits.fromHash)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>fromNumber (value)](#apidoc.element.protobufjs.util.LongBits.fromNumber)
1.  object <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>zero
1.  string <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>zeroHash

#### [module protobufjs.util.LongBits.prototype](#apidoc.module.protobufjs.util.LongBits.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>length ()](#apidoc.element.protobufjs.util.LongBits.prototype.length)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toHash ()](#apidoc.element.protobufjs.util.LongBits.prototype.toHash)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toLong (unsigned)](#apidoc.element.protobufjs.util.LongBits.prototype.toLong)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toNumber (unsigned)](#apidoc.element.protobufjs.util.LongBits.prototype.toNumber)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>zzDecode ()](#apidoc.element.protobufjs.util.LongBits.prototype.zzDecode)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>zzEncode ()](#apidoc.element.protobufjs.util.LongBits.prototype.zzEncode)

#### [module protobufjs.util.ProtocolError](#apidoc.module.protobufjs.util.ProtocolError)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError.ProtocolError)

#### [module protobufjs.util.ProtocolError.prototype](#apidoc.module.protobufjs.util.ProtocolError.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.ProtocolError.prototype.</span>constructor (message, properties)](#apidoc.element.protobufjs.util.ProtocolError.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.ProtocolError.prototype.</span>toString ()](#apidoc.element.protobufjs.util.ProtocolError.prototype.toString)

#### [module protobufjs.util.base64](#apidoc.module.protobufjs.util.base64)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>decode (string, buffer, offset)](#apidoc.element.protobufjs.util.base64.decode)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>encode (buffer, start, end)](#apidoc.element.protobufjs.util.base64.encode)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>length (string)](#apidoc.element.protobufjs.util.base64.length)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>test (string)](#apidoc.element.protobufjs.util.base64.test)

#### [module protobufjs.util.codegen](#apidoc.module.protobufjs.util.codegen)
1.  boolean <span class="apidocSignatureSpan">protobufjs.util.codegen.</span>supported
1.  boolean <span class="apidocSignatureSpan">protobufjs.util.codegen.</span>verbose
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>codegen ()](#apidoc.element.protobufjs.util.codegen.codegen)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.codegen.</span>sprintf (format)](#apidoc.element.protobufjs.util.codegen.sprintf)

#### [module protobufjs.util.fetch](#apidoc.module.protobufjs.util.fetch)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch.fetch)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.fetch.</span>xhr (filename, options, callback)](#apidoc.element.protobufjs.util.fetch.xhr)

#### [module protobufjs.util.float](#apidoc.module.protobufjs.util.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.</span>float (exports)](#apidoc.element.protobufjs.util.float.float)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readDoubleBE (buf, pos)](#apidoc.element.protobufjs.util.float.readDoubleBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readDoubleLE (buf, pos)](#apidoc.element.protobufjs.util.float.readDoubleLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readFloatBE (buf, pos)](#apidoc.element.protobufjs.util.float.readFloatBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readFloatLE (buf, pos)](#apidoc.element.protobufjs.util.float.readFloatLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeDoubleBE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeDoubleBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeDoubleLE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeDoubleLE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeFloatBE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeFloatBE)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeFloatLE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeFloatLE)

#### [module protobufjs.util.path](#apidoc.module.protobufjs.util.path)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.path.</span>isAbsolute (path)](#apidoc.element.protobufjs.util.path.isAbsolute)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.path.</span>normalize (path)](#apidoc.element.protobufjs.util.path.normalize)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.path.</span>resolve (originPath, includePath, alreadyNormalized)](#apidoc.element.protobufjs.util.path.resolve)

#### [module protobufjs.util.toJSONOptions](#apidoc.module.protobufjs.util.toJSONOptions)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>bytes ()](#apidoc.element.protobufjs.util.toJSONOptions.bytes)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>enums ()](#apidoc.element.protobufjs.util.toJSONOptions.enums)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>longs ()](#apidoc.element.protobufjs.util.toJSONOptions.longs)

#### [module protobufjs.util.toJSONOptions.longs.prototype](#apidoc.module.protobufjs.util.toJSONOptions.longs.prototype)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>entityify ()](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.entityify)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>isAlpha ( )](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isAlpha)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>isDigit ()](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isDigit)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>supplant (e)](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.supplant)

#### [module protobufjs.util.utf8](#apidoc.module.protobufjs.util.utf8)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>length (string)](#apidoc.element.protobufjs.util.utf8.length)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>read (buffer, start, end)](#apidoc.element.protobufjs.util.utf8.read)
1.  [function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>write (string, buffer, offset)](#apidoc.element.protobufjs.util.utf8.write)



# <a name="apidoc.module.protobufjs"></a>[module protobufjs](#apidoc.module.protobufjs)

#### <a name="apidoc.element.protobufjs.BufferReader"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>BufferReader (buffer)](#apidoc.element.protobufjs.BufferReader)
- description and source-code
```javascript
function BufferReader(buffer) {
    Reader.call(this, buffer);

    /**
     * Read buffer.
     * @name BufferReader#buf
     * @type {Buffer}
     */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferWriter"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>BufferWriter ()](#apidoc.element.protobufjs.BufferWriter)
- description and source-code
```javascript
function BufferWriter() {
    Writer.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Class"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Class (type, ctor)](#apidoc.element.protobufjs.Class)
- description and source-code
```javascript
function Class(type, ctor) {
    if (!Type)
        Type = require("./type");

    if (!(type instanceof Type))
        throw TypeError("type must be a Type");

    if (ctor) {
        if (typeof ctor !== "function")
            throw TypeError("ctor must be a function");
    } else
        ctor = Class.generate(type).eof(type.name); // named constructor function (codegen is required anyway)

    // Let's pretend...
    ctor.constructor = Class;

    // new Class() -> Message.prototype
    (ctor.prototype = new Message()).constructor = ctor;

    // Static methods on Message are instance methods on Class and vice versa
    util.merge(ctor, Message, true);

    // Classes and messages reference their reflected type
    ctor.$type = type;
    ctor.prototype.$type = type;

    // Messages have non-enumerable default values on their prototype
    var i = 0;
    for (; i < /* initializes */ type.fieldsArray.length; ++i) {
        // objects on the prototype must be immmutable. users must assign a new object instance and
        // cannot use Array#push on empty arrays on the prototype for example, as this would modify
        // the value on the prototype for ALL messages of this type. Hence, these objects are frozen.
        ctor.prototype[type._fieldsArray[i].name] = Array.isArray(type._fieldsArray[i].resolve().defaultValue)
            ? util.emptyArray
            : util.isObject(type._fieldsArray[i].defaultValue) && !type._fieldsArray[i].long
              ? util.emptyObject
              : type._fieldsArray[i].defaultValue; // if a long, it is frozen when initialized
    }

    // Messages have non-enumerable getters and setters for each virtual oneof field
    var ctorProperties = {};
    for (i = 0; i < /* initializes */ type.oneofsArray.length; ++i)
        ctorProperties[type._oneofsArray[i].resolve().name] = {
            get: util.oneOfGetter(type._oneofsArray[i].oneof),
            set: util.oneOfSetter(type._oneofsArray[i].oneof)
        };
    if (i)
        Object.defineProperties(ctor.prototype, ctorProperties);

    // Register
    type.ctor = ctor;

    return ctor.prototype;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Enum"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Enum (name, values, options)](#apidoc.element.protobufjs.Enum)
- description and source-code
```javascript
function Enum(name, values, options) {
    ReflectionObject.call(this, name, options);

    if (values && typeof values !== "object")
        throw TypeError("values must be an object");

    /**
     * Enum values by id.
     * @type {Object.<number,string>}
     */
    this.valuesById = {};

    /**
     * Enum values by name.
     * @type {Object.<string,number>}
     */
    this.values = Object.create(this.valuesById); // toJSON, marker

    /**
     * Value comment texts, if any.
     * @type {Object.<string,string>}
     */
    this.comments = {};

    // Note that values inherit valuesById on their prototype which makes them a TypeScript-
    // compatible enum. This is used by pbts to write actual enum definitions that work for
    // static and reflection code alike instead of emitting generic object definitions.

    if (values)
        for (var keys = Object.keys(values), i = 0; i < keys.length; ++i)
            this.valuesById[ this.values[keys[i]] = values[keys[i]] ] = keys[i];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Field"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Field (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field)
- description and source-code
```javascript
function Field(name, id, type, rule, extend, options) {

    if (util.isObject(rule)) {
        options = rule;
        rule = extend = undefined;
    } else if (util.isObject(extend)) {
        options = extend;
        extend = undefined;
    }

    ReflectionObject.call(this, name, options);

    if (!util.isInteger(id) || id < 0)
        throw TypeError("id must be a non-negative integer");

    if (!util.isString(type))
        throw TypeError("type must be a string");

    if (rule !== undefined && !ruleRe.test(rule = rule.toString().toLowerCase()))
        throw TypeError("rule must be a string rule");

    if (extend !== undefined && !util.isString(extend))
        throw TypeError("extend must be a string");

    /**
     * Field rule, if any.
     * @type {string|undefined}
     */
    this.rule = rule && rule !== "optional" ? rule : undefined; // toJSON

    /**
     * Field type.
     * @type {string}
     */
    this.type = type; // toJSON

    /**
     * Unique field id.
     * @type {number}
     */
    this.id = id; // toJSON, marker

    /**
     * Extended type if different from parent.
     * @type {string|undefined}
     */
    this.extend = extend || undefined; // toJSON

    /**
     * Whether this field is required.
     * @type {boolean}
     */
    this.required = rule === "required";

    /**
     * Whether this field is optional.
     * @type {boolean}
     */
    this.optional = !this.required;

    /**
     * Whether this field is repeated.
     * @type {boolean}
     */
    this.repeated = rule === "repeated";

    /**
     * Whether this field is a map or not.
     * @type {boolean}
     */
    this.map = false;

    /**
     * Message this field belongs to.
     * @type {?Type}
     */
    this.message = null;

    /**
     * OneOf this field belongs to, if any,
     * @type {?OneOf}
     */
    this.partOf = null;

    /**
     * The field type's default value.
     * @type {*}
     */
    this.typeDefault = null;

    /**
     * The field's default value on prototypes.
     * @type {*}
     */
    this.defaultValue = null;

    /**
     * Whether this field's value should be treated as a long.
     * @type {boolean}
     */
    this.long = util.Long ? types.long[type] !== undefined : /* istanbul ignore next */ false;

    /**
     * Whether this field's value is a buffer.
     * @type {boolean}
     */
    this.bytes = type === "bytes";

    /**
     * Resolved type if not a basic type.
     * @type {?(Type|Enum)}
     */
    this.resolvedType = null;

    /**
     * Sister-field within the extended type if a declaring extension field.
     * @type {?Field}
     */
    this.extensionField = null;

    /**
     * Sister-field within the declaring namespace if an extended field.
     * @type {?Field}
     */
    this.declaringField = null;

    /**
     * Internally remembers whether this field is packed.
     * @type {?boolean}
     * @private
     */
    this._packed = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.MapField"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>MapField (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField)
- description and source-code
```javascript
function MapField(name, id, keyType, type, options) {
    Field.call(this, name, id, type, options);

    /* istanbul ignore if */
    if (!util.isString(keyType))
        throw TypeError("keyType must be a string");

    /**
     * Key type.
     * @type {string}
     */
    this.keyType = keyType; // toJSON, marker

    /**
     * Resolved key type if not a basic type.
     * @type {?ReflectionObject}
     */
    this.resolvedKeyType = null;

    // Overrides Field#map
    this.map = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Message (properties)](#apidoc.element.protobufjs.Message)
- description and source-code
```javascript
function Message(properties) {
    // not used internally
    if (properties)
        for (var keys = Object.keys(properties), i = 0; i < keys.length; ++i)
            this[keys[i]] = properties[keys[i]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Method"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Method (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method)
- description and source-code
```javascript
function Method(name, type, requestType, responseType, requestStream, responseStream, options) {

    /* istanbul ignore next */
    if (util.isObject(requestStream)) {
        options = requestStream;
        requestStream = responseStream = undefined;
    } else if (util.isObject(responseStream)) {
        options = responseStream;
        responseStream = undefined;
    }

    /* istanbul ignore if */
    if (!(type === undefined || util.isString(type)))
        throw TypeError("type must be a string");

    /* istanbul ignore if */
    if (!util.isString(requestType))
        throw TypeError("requestType must be a string");

    /* istanbul ignore if */
    if (!util.isString(responseType))
        throw TypeError("responseType must be a string");

    ReflectionObject.call(this, name, options);

    /**
     * Method type.
     * @type {string}
     */
    this.type = type || "rpc"; // toJSON

    /**
     * Request type.
     * @type {string}
     */
    this.requestType = requestType; // toJSON, marker

    /**
     * Whether requests are streamed or not.
     * @type {boolean|undefined}
     */
    this.requestStream = requestStream ? true : undefined; // toJSON

    /**
     * Response type.
     * @type {string}
     */
    this.responseType = responseType; // toJSON

    /**
     * Whether responses are streamed or not.
     * @type {boolean|undefined}
     */
    this.responseStream = responseStream ? true : undefined; // toJSON

    /**
     * Resolved request type.
     * @type {?Type}
     */
    this.resolvedRequestType = null;

    /**
     * Resolved response type.
     * @type {?Type}
     */
    this.resolvedResponseType = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Namespace (name, options)](#apidoc.element.protobufjs.Namespace)
- description and source-code
```javascript
function Namespace(name, options) {
    ReflectionObject.call(this, name, options);

    /**
     * Nested objects by name.
     * @type {Object.<string,ReflectionObject>|undefined}
     */
    this.nested = undefined; // toJSON

    /**
     * Cached nested objects as an array.
     * @type {?ReflectionObject[]}
     * @private
     */
    this._nestedArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>OneOf (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf)
- description and source-code
```javascript
function OneOf(name, fieldNames, options) {
    if (!Array.isArray(fieldNames)) {
        options = fieldNames;
        fieldNames = undefined;
    }
    ReflectionObject.call(this, name, options);

    /* istanbul ignore if */
    if (!(fieldNames === undefined || Array.isArray(fieldNames)))
        throw TypeError("fieldNames must be an Array");

    /**
     * Field names that belong to this oneof.
     * @type {string[]}
     */
    this.oneof = fieldNames || []; // toJSON, marker

    /**
     * Fields that belong to this oneof as an array for iteration.
     * @type {Field[]}
     * @readonly
     */
    this.fieldsArray = []; // declared readonly for conformance, possibly not yet added to parent
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Reader (buffer)](#apidoc.element.protobufjs.Reader)
- description and source-code
```javascript
function Reader(buffer) {

    /**
     * Read buffer.
     * @type {Uint8Array}
     */
    this.buf = buffer;

    /**
     * Read buffer position.
     * @type {number}
     */
    this.pos = 0;

    /**
     * Read buffer length.
     * @type {number}
     */
    this.len = buffer.length;
}
```
- example usage
```shell
...

if (process.argv.length > 3 && /^\d+$/.test(process.argv[3]))
count = parseInt(process.argv[3], 10);
process.stdout.write(" x " + count + "\n");

function setupBrowser() {
protobuf.Writer.create = function create_browser() { return new protobuf.Writer(); };
protobuf.Reader.create = function create_browser(buf) { return new protobuf.Reader(buf); };
}

switch (process.argv[2]) {
case "encode-browser":
    setupBrowser();
    // eslint-disable-line no-fallthrough
case "encode":
...
```

#### <a name="apidoc.element.protobufjs.ReflectionObject"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>ReflectionObject (name, options)](#apidoc.element.protobufjs.ReflectionObject)
- description and source-code
```javascript
function ReflectionObject(name, options) {

    if (!util.isString(name))
        throw TypeError("name must be a string");

    if (options && !util.isObject(options))
        throw TypeError("options must be an object");

    /**
     * Options.
     * @type {Object.<string,*>|undefined}
     */
    this.options = options; // toJSON

    /**
     * Unique name within its namespace.
     * @type {string}
     */
    this.name = name;

    /**
     * Parent namespace.
     * @type {?Namespace}
     */
    this.parent = null;

    /**
     * Whether already resolved or not.
     * @type {boolean}
     */
    this.resolved = false;

    /**
     * Comment text, if any.
     * @type {?string}
     */
    this.comment = null;

    /**
     * Defining file name.
     * @type {?string}
     */
    this.filename = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Root (options)](#apidoc.element.protobufjs.Root)
- description and source-code
```javascript
function Root(options) {
    Namespace.call(this, "", options);

    /**
     * Deferred extension fields.
     * @type {Field[]}
     */
    this.deferred = [];

    /**
     * Resolved file names of loaded files.
     * @type {string[]}
     */
    this.files = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Service"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Service (name, options)](#apidoc.element.protobufjs.Service)
- description and source-code
```javascript
function Service(name, options) {
    Namespace.call(this, name, options);

    /**
     * Service methods.
     * @type {Object.<string,Method>}
     */
    this.methods = {}; // toJSON, marker

    /**
     * Cached methods as an array.
     * @type {?Method[]}
     * @private
     */
    this._methodsArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Type (name, options)](#apidoc.element.protobufjs.Type)
- description and source-code
```javascript
function Type(name, options) {
    Namespace.call(this, name, options);

    /**
     * Message fields.
     * @type {Object.<string,Field>}
     */
    this.fields = {};  // toJSON, marker

    /**
     * Oneofs declared within this namespace, if any.
     * @type {Object.<string,OneOf>}
     */
    this.oneofs = undefined; // toJSON

    /**
     * Extension ranges, if any.
     * @type {number[][]}
     */
    this.extensions = undefined; // toJSON

    /**
     * Reserved ranges, if any.
     * @type {Array.<number[]|string>}
     */
    this.reserved = undefined; // toJSON

    /*?
     * Whether this type is a legacy group.
     * @type {boolean|undefined}
     */
    this.group = undefined; // toJSON

    /**
     * Cached fields by id.
     * @type {?Object.<number,Field>}
     * @private
     */
    this._fieldsById = null;

    /**
     * Cached fields as an array.
     * @type {?Field[]}
     * @private
     */
    this._fieldsArray = null;

    /**
     * Cached oneofs as an array.
     * @type {?OneOf[]}
     * @private
     */
    this._oneofsArray = null;

    /**
     * Cached constructor.
     * @type {*}
     * @private
     */
    this._ctor = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Writer ()](#apidoc.element.protobufjs.Writer)
- description and source-code
```javascript
function Writer() {

    /**
     * Current length.
     * @type {number}
     */
    this.len = 0;

    /**
     * Operations head.
     * @type {Object}
     */
    this.head = new Op(noop, 0, 0);

    /**
     * Operations tail
     * @type {Object}
     */
    this.tail = this.head;

    /**
     * Linked forked states.
     * @type {?Object}
     */
    this.states = null;

    // When a value is written, the writer calculates its byte length and puts it into a linked
    // list of operations to perform when finish() is called. This both allows us to allocate
    // buffers of the exact required size and reduces the amount of work we have to do compared
    // to first calculating over objects and then encoding over objects. In our case, the encoding
    // part is just a linked list walk calling operations with already prepared values.
}
```
- example usage
```shell
...
}

if (process.argv.length > 3 && /^\d+$/.test(process.argv[3]))
count = parseInt(process.argv[3], 10);
process.stdout.write(" x " + count + "\n");

function setupBrowser() {
protobuf.Writer.create = function create_browser() { return new protobuf.Writer(); };
protobuf.Reader.create = function create_browser(buf) { return new protobuf.Reader(buf); };
}

switch (process.argv[2]) {
case "encode-browser":
    setupBrowser();
    // eslint-disable-line no-fallthrough
...
```

#### <a name="apidoc.element.protobufjs.common"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>common (name, json)](#apidoc.element.protobufjs.common)
- description and source-code
```javascript
function common(name, json) {
    if (!commonRe.test(name)) {
        name = "google/protobuf/" + name + ".proto";
        json = { nested: { google: { nested: { protobuf: { nested: json } } } } };
    }
    common[name] = json;
}
```
- example usage
```shell
...
 * @property {Object.<string,*>} google/protobuf/duration.proto Duration
 * @property {Object.<string,*>} google/protobuf/empty.proto Empty
 * @property {Object.<string,*>} google/protobuf/struct.proto Struct, Value, NullValue and ListValue
 * @property {Object.<string,*>} google/protobuf/timestamp.proto Timestamp
 * @property {Object.<string,*>} google/protobuf/wrappers.proto Wrappers
 * @example
 * // manually provides descriptor.proto (assumes google/protobuf/ namespace and .proto extension)
 * protobuf.common("descriptor", descriptorJson);
 *
 * // manually provides a custom definition (uses my.foo namespace)
 * protobuf.common("my/foo/bar.proto", myFooBarJson);
 */
function common(name, json) {
if (!commonRe.test(name)) {
    name = "google/protobuf/" + name + ".proto";
...
```

#### <a name="apidoc.element.protobufjs.configure"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>configure ()](#apidoc.element.protobufjs.configure)
- description and source-code
```javascript
function configure() {
    protobuf.Reader._configure(protobuf.BufferReader);
    protobuf.util._configure();
}
```
- example usage
```shell
...
var protobuf = global.protobuf = $require(entries[0]);

// Be nice to AMD
if (typeof define === "function" && define.amd)
    define(["long"], function(Long) {
        if (Long && Long.isLong) {
            protobuf.util.Long = Long;
            protobuf.configure();
        }
        return protobuf;
    });

// Be nice to CommonJS
if (typeof module === "object" && module && module.exports)
    module.exports = protobuf;
...
```

#### <a name="apidoc.element.protobufjs.decoder"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>decoder (mtype)](#apidoc.element.protobufjs.decoder)
- description and source-code
```javascript
function decoder(mtype) {
    /* eslint-disable no-unexpected-multiline */
    var gen = util.codegen("r", "l")
    ("if(!(r instanceof Reader))")
        ("r=Reader.create(r)")
    ("var c=l===undefined?r.len:r.pos+l,m=new this.ctor" + (mtype.fieldsArray.filter(function(field) { return field.map; }).length
 ? ",k" : ""))
    ("while(r.pos<c){")
        ("var t=r.uint32()");
    if (mtype.group) gen
        ("if((t&7)===4)")
            ("break");
    gen
        ("switch(t>>>3){");

    var i = 0;
    for (; i < /* initializes */ mtype.fieldsArray.length; ++i) {
        var field = mtype._fieldsArray[i].resolve(),
            type  = field.resolvedType instanceof Enum ? "uint32" : field.type,
            ref   = "m" + util.safeProp(field.name); gen
            ("case %d:", field.id);

        // Map fields
        if (field.map) { gen
                ("r.skip().pos++") // assumes id 1 + key wireType
                ("if(%s===util.emptyObject)", ref)
                    ("%s={}", ref)
                ("k=r.%s()", field.keyType)
                ("r.pos++"); // assumes id 2 + value wireType
            if (types.long[field.keyType] !== undefined) {
                if (types.basic[type] === undefined) gen
                ("%s[typeof k===\"object\"?util.longToHash(k):k]=types[%d].decode(r,r.uint32())", ref, i); // can't be groups
                else gen
                ("%s[typeof k===\"object\"?util.longToHash(k):k]=r.%s()", ref, type);
            } else {
                if (types.basic[type] === undefined) gen
                ("%s[k]=types[%d].decode(r,r.uint32())", ref, i); // can't be groups
                else gen
                ("%s[k]=r.%s()", ref, type);
            }

        // Repeated fields
        } else if (field.repeated) { gen

                ("if(!(%s&&%s.length))", ref, ref)
                    ("%s=[]", ref);

            // Packable (always check for forward and backward compatiblity)
            if (types.packed[type] !== undefined) gen
                ("if((t&7)===2){")
                    ("var c2=r.uint32()+r.pos")
                    ("while(r.pos<c2)")
                        ("%s.push(r.%s())", ref, type)
                ("}else");

            // Non-packed
            if (types.basic[type] === undefined) gen(field.resolvedType.group
                    ? "%s.push(types[%d].decode(r))"
                    : "%s.push(types[%d].decode(r,r.uint32()))", ref, i);
            else gen
                    ("%s.push(r.%s())", ref, type);

        // Non-repeated
        } else if (types.basic[type] === undefined) gen(field.resolvedType.group
                ? "%s=types[%d].decode(r)"
                : "%s=types[%d].decode(r,r.uint32())", ref, i);
        else gen
                ("%s=r.%s()", ref, type);
        gen
                ("break");
    // Unknown fields
    } gen
            ("default:")
                ("r.skipType(t&7)")
                ("break")

        ("}")
    ("}");

    // Field presence
    for (i = 0; i < mtype._fieldsArray.length; ++i) {
        var rfield = mtype._fieldsArray[i];
        if (rfield.required) gen
    ("if(!m.hasOwnProperty(%j))", rfield.name)
        ("throw util.ProtocolError(%j,{instance:m})", missing(rfield));
    }

    return gen
    ("return m");
    /* eslint-enable no-unexpected-multiline */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.encoder"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>encoder (mtype)](#apidoc.element.protobufjs.encoder)
- description and source-code
```javascript
function encoder(mtype) {
    /* eslint-disable no-unexpected-multiline, block-scoped-var, no-redeclare */
    var gen = util.codegen("m", "w")
    ("if(!w)")
        ("w=Writer.create()");

    var i, ref;

    // "when a message is serialized its known fields should be written sequentially by field number"
    var fields = /* initializes */ mtype.fieldsArray.slice().sort(util.compareFieldsById);

    for (var i = 0; i < fields.length; ++i) {
        var field    = fields[i].resolve(),
            index    = mtype._fieldsArray.indexOf(field),
            type     = field.resolvedType instanceof Enum ? "uint32" : field.type,
            wireType = types.basic[type];
            ref      = "m" + util.safeProp(field.name);

        // Map fields
        if (field.map) {
            gen
    ("if(%s&&m.hasOwnProperty(%j)){", ref, field.name)
        ("for(var ks=Object.keys(%s),i=0;i<ks.length;++i){", ref)
            ("w.uint32(%d).fork().uint32(%d).%s(ks[i])", (field.id << 3 | 2) >>> 0, 8 | types.mapKey[field.keyType], field.keyType
);
            if (wireType === undefined) gen
            ("types[%d].encode(%s[ks[i]],w.uint32(18).fork()).ldelim().ldelim()", index, ref); // can't be groups
            else gen
            (".uint32(%d).%s(%s[ks[i]]).ldelim()", 16 | wireType, type, ref);
            gen
        ("}")
    ("}");

            // Repeated fields
        } else if (field.repeated) { gen
    ("if(%s&&%s.length){", ref, ref);

            // Packed repeated
            if (field.packed && types.packed[type] !== undefined) { gen

        ("w.uint32(%d).fork()", (field.id << 3 | 2) >>> 0)
        ("for(var i=0;i<%s.length;++i)", ref)
            ("w.%s(%s[i])", type, ref)
        ("w.ldelim()");

            // Non-packed
            } else { gen

        ("for(var i=0;i<%s.length;++i)", ref);
                if (wireType === undefined)
            genTypePartial(gen, field, index, ref + "[i]");
                else gen
            ("w.uint32(%d).%s(%s[i])", (field.id << 3 | wireType) >>> 0, type, ref);

            } gen
    ("}");

        // Non-repeated
        } else {
            if (field.optional) {

                if (field.bytes || field.resolvedType && !(field.resolvedType instanceof Enum)) gen
    ("if(%s&&m.hasOwnProperty(%j))", ref, field.name);
                else gen
    ("if(%s!=null&&m.hasOwnProperty(%j))", ref, field.name); // !== undefined && !== null

            }

            if (wireType === undefined)
        genTypePartial(gen, field, index, ref);
            else gen
        ("w.uint32(%d).%s(%s)", (field.id << 3 | wireType) >>> 0, type, ref);

        }
    }

    return gen
    ("return w");
    /* eslint-enable no-unexpected-multiline, block-scoped-var, no-redeclare */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.load"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>load (filename, root, callback)](#apidoc.element.protobufjs.load)
- description and source-code
```javascript
function load(filename, root, callback) {
    if (typeof root === "function") {
        callback = root;
        root = new protobuf.Root();
    } else if (!root)
        root = new protobuf.Root();
    return root.load(filename, callback);
}
```
- example usage
```shell
...

message AwesomeMessage {
string awesome_field = 1; // becomes awesomeField
}
'''

'''js
protobuf.load("awesome.proto", function(err, root) {
if (err)
    throw err;

// Obtain a message type
var AwesomeMessage = root.lookupType("awesomepackage.AwesomeMessage");

// Exemplary payload
...
```

#### <a name="apidoc.element.protobufjs.loadSync"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>loadSync (filename, root)](#apidoc.element.protobufjs.loadSync)
- description and source-code
```javascript
function loadSync(filename, root) {
    if (!root)
        root = new protobuf.Root();
    return root.loadSync(filename);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.parse"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>parse (source, root, options)](#apidoc.element.protobufjs.parse)
- description and source-code
```javascript
function parse(source, root, options) {
    /* eslint-disable callback-return */
    if (!(root instanceof Root)) {
        options = root;
        root = new Root();
    }
    if (!options)
        options = parse.defaults;

    var tn = tokenize(source),
        next = tn.next,
        push = tn.push,
        peek = tn.peek,
        skip = tn.skip,
        cmnt = tn.cmnt;

    var head = true,
        pkg,
        imports,
        weakImports,
        syntax,
        isProto3 = false;

    var ptr = root;

    var applyCase = options.keepCase ? function(name) { return name; } : camelCase;

    /* istanbul ignore next */
    function illegal(token, name, insideTryCatch) {
        var filename = parse.filename;
        if (!insideTryCatch)
            parse.filename = null;
        return Error("illegal " + (name || "token") + " '" + token + "' (" + (filename ? filename + ", " : "") + "line " + tn.line
() + ")");
    }

    function readString() {
        var values = [],
            token;
        do {
            /* istanbul ignore if */
            if ((token = next()) !== "\"" && token !== "'")
                throw illegal(token);

            values.push(next());
            skip(token);
            token = peek();
        } while (token === "\"" || token === "'");
        return values.join("");
    }

    function readValue(acceptTypeRef) {
        var token = next();
        switch (token) {
            case "'":
            case "\"":
                push(token);
                return readString();
            case "true": case "TRUE":
                return true;
            case "false": case "FALSE":
                return false;
        }
        try {
            return parseNumber(token, /* insideTryCatch */ true);
        } catch (e) {

            /* istanbul ignore else */
            if (acceptTypeRef && typeRefRe.test(token))
                return token;

            /* istanbul ignore next */
            throw illegal(token, "value");
        }
    }

    function readRanges(target, acceptStrings) {
        var token, start;
        do {
            if (acceptStrings && ((token = peek()) === "\"" || token === "'"))
                target.push(readString());
            else
                target.push([ start = parseId(next()), skip("to", true) ? parseId(next()) : start ]);
        } while (skip(",", true));
        skip(";");
    }

    function parseNumber(token, insideTryCatch) {
        var sign = 1;
        if (token.charAt(0) === "-") {
            sign = -1;
            token = token.substring(1);
        }
        switch (token) {
            case "inf": case "INF": case "Inf":
                return sign * Infinity;
            case "nan": case "NAN": case "Nan": case "NaN":
                return NaN;
            case "0":
                return 0;
        }
        if (base10Re.test(token))
            return sign * parseInt(token, 10);
        if (base16Re.test(token))
            return sign * parseInt(token, 16);
        if (base8Re.test(token))
            return sign * parseInt(token, 8);

        /* istanbul ignore else */
        if (numberRe.test(token))
            return sign * parseFloat(token);

        /* istanbul ignore next */
        throw illegal(token, "number", insideTryCatch);
    }

    function parseId(token, acceptNegative) {
        switch (token) {
            case "max": case "MAX": case "Max":
                return 536870911;
            case "0":
                return 0;
        }

        /* istanbul ignore if */
        if (!acceptNegative && token.charAt(0) === "-")
            throw illegal(token, "id");

        if (base10NegRe.test(token))
            return parseInt(token, 10);
        if (base16NegRe.test(token))
            return parseInt(token, 16);

        /* istanbul ignore else */
        if (base8NegRe.test(token))
            return parseInt(token, 8);

        /* istanbul ignore next */
        throw illeg ...
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.rpc.Service"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>rpc.Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service)
- description and source-code
```javascript
function Service(rpcImpl, requestDelimited, responseDelimited) {

    if (typeof rpcImpl !== "function")
        throw TypeError("rpcImpl must be a function");

    util.EventEmitter.call(this);

    /**
     * RPC implementation. Becomes 'null' once the service is ended.
     * @type {?RPCImpl}
     */
    this.rpcImpl = rpcImpl;

    /**
     * Whether requests are length-delimited.
     * @type {boolean}
     */
    this.requestDelimited = Boolean(requestDelimited);

    /**
     * Whether responses are length-delimited.
     * @type {boolean}
     */
    this.responseDelimited = Boolean(responseDelimited);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.tokenize"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>tokenize (source)](#apidoc.element.protobufjs.tokenize)
- description and source-code
```javascript
function tokenize(source) {
    /* eslint-disable callback-return */
    source = source.toString();

    var offset = 0,
        length = source.length,
        line = 1,
        commentType = null,
        commentText = null,
        commentLine = 0;

    var stack = [];

    var stringDelim = null;

    /* istanbul ignore next */
    /**
     * Creates an error for illegal syntax.
     * @param {string} subject Subject
     * @returns {Error} Error created
     * @inner
     */
    function illegal(subject) {
        return Error("illegal " + subject + " (line " + line + ")");
    }

    /**
     * Reads a string till its end.
     * @returns {string} String read
     * @inner
     */
    function readString() {
        var re = stringDelim === "'" ? stringSingleRe : stringDoubleRe;
        re.lastIndex = offset - 1;
        var match = re.exec(source);
        if (!match)
            throw illegal("string");
        offset = re.lastIndex;
        push(stringDelim);
        stringDelim = null;
        return unescape(match[1]);
    }

    /**
     * Gets the character at 'pos' within the source.
     * @param {number} pos Position
     * @returns {string} Character
     * @inner
     */
    function charAt(pos) {
        return source.charAt(pos);
    }

    /**
     * Sets the current comment text.
     * @param {number} start Start offset
     * @param {number} end End offset
     * @returns {undefined}
     * @inner
     */
    function setComment(start, end) {
        commentType = source.charAt(start++);
        commentLine = line;
        var lines = source
            .substring(start, end)
            .split(setCommentSplitRe);
        for (var i = 0; i < lines.length; ++i)
            lines[i] = lines[i].replace(setCommentRe, "").trim();
        commentText = lines
            .join("\n")
            .trim();
    }

    /**
     * Obtains the next token.
     * @returns {?string} Next token or 'null' on eof
     * @inner
     */
    function next() {
        if (stack.length > 0)
            return stack.shift();
        if (stringDelim)
            return readString();
        var repeat,
            prev,
            curr,
            start,
            isComment;
        do {
            if (offset === length)
                return null;
            repeat = false;
            while (whitespaceRe.test(curr = charAt(offset))) {
                if (curr === "\n")
                    ++line;
                if (++offset === length)
                    return null;
            }
            if (charAt(offset) === "/") {
                if (++offset === length)
                    throw illegal("comment");
                if (charAt(offset) === "/") { // Line
                    isComment = charAt(start = offset + 1) === "/";
                    while (charAt(++offset) !== "\n")
                        if (offset === length)
                            return null;
                    ++offset;
                    if (isComment)
                        setComment(start, offset - 1);
                    ++line;
                    repeat = true;
                } else if ((curr = charAt(offset)) === "*") { /* Block */
                    isComment = charAt(start = offset + 1) === "*";
                    do {
                        if (curr === "\n")
                            ++line;
                        if (++offset === length)
                            throw illegal("comment");
                        prev = curr;
                        curr = charAt(offset);
                    } while (prev !== "*" || curr !== "/");
                    ++offset;
                    if (isComment)
                        setComment(start, offset - 2);
                    repeat = true;
                } else
                    return "/";
            }
        } while (repeat);

        // offset !== length if we got here

        var end = offset;
        delimRe.lastIndex = 0; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.EventEmitter"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {

    /**
     * Registered listeners.
     * @type {Object.<string,*>}
     * @private
     */
    this._listeners = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long)
- description and source-code
```javascript
function Long(low, high, unsigned) {

    /**
     * The low 32 bits as a signed value.
     * @type {number}
     */
    this.low = low | 0;

    /**
     * The high 32 bits as a signed value.
     * @type {number}
     */
    this.high = high | 0;

    /**
     * Whether unsigned or not.
     * @type {boolean}
     */
    this.unsigned = !!unsigned;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits)
- description and source-code
```javascript
function LongBits(lo, hi) {

    // note that the casts below are theoretically unnecessary as of today, but older statically
    // generated converter code might still call the ctor with signed 32bits. kept for compat.

    /**
     * Low bits.
     * @type {number}
     */
    this.lo = lo >>> 0;

    /**
     * High bits.
     * @type {number}
     */
    this.hi = hi >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.ProtocolError"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError)
- description and source-code
```javascript
function CustomError(message, properties) {

    if (!(this instanceof CustomError))
        return new CustomError(message, properties);

    // Error.call(this, message);
    // ^ just returns a new error instance because the ctor can be called as a function

    Object.defineProperty(this, "message", { get: function() { return message; } });

    /* istanbul ignore next */
    if (Error.captureStackTrace) // node
        Error.captureStackTrace(this, CustomError);
    else
        Object.defineProperty(this, "stack", { value: (new Error()).stack || "" });

    if (properties)
        merge(this, properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.codegen"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.codegen ()](#apidoc.element.protobufjs.util.codegen)
- description and source-code
```javascript
function codegen() {
    var params = [],
        src    = [],
        indent = 1,
        inCase = false;
    for (var i = 0; i < arguments.length;)
        params.push(arguments[i++]);

    /**
     * A codegen instance as returned by {@link codegen}, that also is a sprintf-like appender function.
     * @typedef Codegen
     * @type {function}
     * @param {string} format Format string
     * @param {...*} args Replacements
     * @returns {Codegen} Itself
     * @property {function(string=):string} str Stringifies the so far generated function source.
     * @property {function(string=, Object=):function} eof Ends generation and builds the function whilst applying a scope.
     */
    /**/
    function gen() {
        var args = [],
            i = 0;
        for (; i < arguments.length;)
            args.push(arguments[i++]);
        var line = sprintf.apply(null, args);
        var level = indent;
        if (src.length) {
            var prev = src[src.length - 1];

            // block open or one time branch
            if (blockOpenRe.test(prev))
                level = ++indent; // keep
            else if (branchRe.test(prev))
                ++level; // once

            // casing
            if (casingRe.test(prev) && !casingRe.test(line)) {
                level = ++indent;
                inCase = true;
            } else if (inCase && breakRe.test(prev)) {
                level = --indent;
                inCase = false;
            }

            // block close
            if (blockCloseRe.test(line))
                level = --indent;
        }
        for (i = 0; i < level; ++i)
            line = "\t" + line;
        src.push(line);
        return gen;
    }

    /**
     * Stringifies the so far generated function source.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @returns {string} Function source using tabs for indentation
     * @inner
     */
    function str(name) {
        return "function" + (name ? " " + name.replace(/[^\w_$]/g, "_") : "") + "(" + params.join(",") + ") {\n" + src.join("\n") + "\n}";
    }

    gen.str = str;

    /**
     * Ends generation and builds the function whilst applying a scope.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @param {Object.<string,*>} [scope] Function scope
     * @returns {function} The generated function, with scope applied if specified
     * @inner
     */
    function eof(name, scope) {
        if (typeof name === "object") {
            scope = name;
            name = undefined;
        }
        var source = gen.str(name);
        if (codegen.verbose)
            console.log("--- codegen ---\n" + source.replace(/^/mg, "> ").replace(/\t/g, "  ")); // eslint-disable-line no-console
        var keys = Object.keys(scope || (scope = {}));
        return Function.apply(null, keys.concat("return " + source)).apply(null, keys.map(function(key) { return scope[key]; })); //
eslint-disable-line no-new-func
        //     ^ Creates a wrapper function with the scoped variable names as its parameters,
        //       calls it with the respective scoped variable values ^
        //       and returns our brand-new properly scoped function.
        //
        // This works because "Invoking the Function constructor as a function (without using the
        // new operator) has the same effect as invoking it as a constructor."
        // https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Function
    }

    gen.eof = eof;

    return gen;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.fetch"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch)
- description and source-code
```javascript
function fetch(filename, options, callback) {
    if (typeof options === "function") {
        callback = options;
        options = {};
    } else if (!options)
        options = {};

    if (!callback)
        return asPromise(fetch, this, filename, options); // eslint-disable-line no-invalid-this

    // if a node-like filesystem is present, try it first but fall back to XHR if nothing is found.
    if (!options.xhr && fs && fs.readFile)
        return fs.readFile(filename, function fetchReadFileCallback(err, contents) {
            return err && typeof XMLHttpRequest !== "undefined"
                ? fetch.xhr(filename, options, callback)
                : err
                ? callback(err)
                : callback(null, options.binary ? contents : contents.toString("utf8"));
        });

    // use the XHR version otherwise.
    return fetch.xhr(filename, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>util.float (exports)](#apidoc.element.protobufjs.util.float)
- description and source-code
```javascript
function factory(exports) {

    // float: typed array
    if (typeof Float32Array !== "undefined") (function() {

        var f32 = new Float32Array([ -0 ]),
            f8b = new Uint8Array(f32.buffer),
            le  = f8b[3] === 128;

        function writeFloat_f32_cpy(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
        }

        function writeFloat_f32_rev(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[3];
            buf[pos + 1] = f8b[2];
            buf[pos + 2] = f8b[1];
            buf[pos + 3] = f8b[0];
        }

        /* istanbul ignore next */
        exports.writeFloatLE = le ? writeFloat_f32_cpy : writeFloat_f32_rev;
        /* istanbul ignore next */
        exports.writeFloatBE = le ? writeFloat_f32_rev : writeFloat_f32_cpy;

        function readFloat_f32_cpy(buf, pos) {
            f8b[0] = buf[pos    ];
            f8b[1] = buf[pos + 1];
            f8b[2] = buf[pos + 2];
            f8b[3] = buf[pos + 3];
            return f32[0];
        }

        function readFloat_f32_rev(buf, pos) {
            f8b[3] = buf[pos    ];
            f8b[2] = buf[pos + 1];
            f8b[1] = buf[pos + 2];
            f8b[0] = buf[pos + 3];
            return f32[0];
        }

        /* istanbul ignore next */
        exports.readFloatLE = le ? readFloat_f32_cpy : readFloat_f32_rev;
        /* istanbul ignore next */
        exports.readFloatBE = le ? readFloat_f32_rev : readFloat_f32_cpy;

    // float: ieee754
    })(); else (function() {

        function writeFloat_ieee754(writeUint, val, buf, pos) {
            var sign = val < 0 ? 1 : 0;
            if (sign)
                val = -val;
            if (val === 0)
                writeUint(1 / val > 0 ? /* positive */ 0 : /* negative 0 */ 2147483648, buf, pos);
            else if (isNaN(val))
                writeUint(2143289344, buf, pos);
            else if (val > 3.4028234663852886e+38) // +-Infinity
                writeUint((sign << 31 | 2139095040) >>> 0, buf, pos);
            else if (val < 1.1754943508222875e-38) // denormal
                writeUint((sign << 31 | Math.round(val / 1.401298464324817e-45)) >>> 0, buf, pos);
            else {
                var exponent = Math.floor(Math.log(val) / Math.LN2),
                    mantissa = Math.round(val * Math.pow(2, -exponent) * 8388608) & 8388607;
                writeUint((sign << 31 | exponent + 127 << 23 | mantissa) >>> 0, buf, pos);
            }
        }

        exports.writeFloatLE = writeFloat_ieee754.bind(null, writeUintLE);
        exports.writeFloatBE = writeFloat_ieee754.bind(null, writeUintBE);

        function readFloat_ieee754(readUint, buf, pos) {
            var uint = readUint(buf, pos),
                sign = (uint >> 31) * 2 + 1,
                exponent = uint >>> 23 & 255,
                mantissa = uint & 8388607;
            return exponent === 255
                ? mantissa
                ? NaN
                : sign * Infinity
                : exponent === 0 // denormal
                ? sign * 1.401298464324817e-45 * mantissa
                : sign * Math.pow(2, exponent - 150) * (mantissa + 8388608);
        }

        exports.readFloatLE = readFloat_ieee754.bind(null, readUintLE);
        exports.readFloatBE = readFloat_ieee754.bind(null, readUintBE);

    })();

    // double: typed array
    if (typeof Float64Array !== "undefined") (function() {

        var f64 = new Float64Array([-0]),
            f8b = new Uint8Array(f64.buffer),
            le  = f8b[7] === 128;

        function writeDouble_f64_cpy(val, buf, pos) {
            f64[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
            buf[pos + 4] = f8b[4];
            buf[pos + 5] = f8b[5];
            buf[pos + 6] = f8b[6] ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.verifier"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>verifier (mtype)](#apidoc.element.protobufjs.verifier)
- description and source-code
```javascript
function verifier(mtype) {
    /* eslint-disable no-unexpected-multiline */

    var gen = util.codegen("m")
    ("if(typeof m!==\"object\"||m===null)")
        ("return%j", "object expected");
    var oneofs = mtype.oneofsArray,
        seenFirstField = {};
    if (oneofs.length) gen
    ("var p={}");

    for (var i = 0; i < /* initializes */ mtype.fieldsArray.length; ++i) {
        var field = mtype._fieldsArray[i].resolve(),
            ref   = "m" + util.safeProp(field.name);

        // map fields
        if (field.map) { gen
            ("if(%s!=null){", ref) // !== undefined && !== null
                ("if(!util.isObject(%s))", ref)
                    ("return%j", invalid(field, "object"))
                ("var k=Object.keys(%s)", ref)
                ("for(var i=0;i<k.length;++i){");
                    genVerifyKey(gen, field, "k[i]");
                    genVerifyValue(gen, field, i, ref + "[k[i]]")
                ("}")
            ("}");

        // repeated fields
        } else if (field.repeated) { gen
            ("if(%s!=null){", ref) // !== undefined && !== null
                ("if(!Array.isArray(%s))", ref)
                    ("return%j", invalid(field, "array"))
                ("for(var i=0;i<%s.length;++i){", ref);
                    genVerifyValue(gen, field, i, ref + "[i]")
                ("}")
            ("}");

        // required or present fields
        } else {
            if (field.optional) gen
            ("if(%s!=null){", ref); // !== undefined && !== null
            if (field.partOf) {
                var oneofProp = util.safeProp(field.partOf.name);
                if (seenFirstField[field.partOf.name] === 1) gen
            ("if(p%s===1)", oneofProp)
                ("return%j", field.partOf.name + ": multiple values");
                seenFirstField[field.partOf.name] = 1;
                gen
            ("p%s=1", oneofProp);
            }
                genVerifyValue(gen, field, i, ref);
            if (field.optional) gen
            ("}");
        }
    } return gen
    ("return null");
    /* eslint-enable no-unexpected-multiline */
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.BufferReader"></a>[module protobufjs.BufferReader](#apidoc.module.protobufjs.BufferReader)

#### <a name="apidoc.element.protobufjs.BufferReader.BufferReader"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>BufferReader (buffer)](#apidoc.element.protobufjs.BufferReader.BufferReader)
- description and source-code
```javascript
function BufferReader(buffer) {
    Reader.call(this, buffer);

    /**
     * Read buffer.
     * @name BufferReader#buf
     * @type {Buffer}
     */
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.BufferReader.prototype"></a>[module protobufjs.BufferReader.prototype](#apidoc.module.protobufjs.BufferReader.prototype)

#### <a name="apidoc.element.protobufjs.BufferReader.prototype._slice"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>_slice (start, end)](#apidoc.element.protobufjs.BufferReader.prototype._slice)
- description and source-code
```javascript
function slice(start, end) {
  const srcLength = this.length;
  start = adjustOffset(start, srcLength);
  end = end !== undefined ? adjustOffset(end, srcLength) : srcLength;
  const newLength = end > start ? end - start : 0;
  return new FastBuffer(this.buffer, this.byteOffset + start, newLength);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferReader.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>constructor (buffer)](#apidoc.element.protobufjs.BufferReader.prototype.constructor)
- description and source-code
```javascript
function BufferReader(buffer) {
    Reader.call(this, buffer);

    /**
     * Read buffer.
     * @name BufferReader#buf
     * @type {Buffer}
     */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferReader.prototype.string"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferReader.prototype.</span>string ()](#apidoc.element.protobufjs.BufferReader.prototype.string)
- description and source-code
```javascript
function read_string_buffer() {
    var len = this.uint32(); // modifies pos
    return this.buf.utf8Slice(this.pos, this.pos = Math.min(this.pos + len, this.len));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.BufferWriter"></a>[module protobufjs.BufferWriter](#apidoc.module.protobufjs.BufferWriter)

#### <a name="apidoc.element.protobufjs.BufferWriter.BufferWriter"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>BufferWriter ()](#apidoc.element.protobufjs.BufferWriter.BufferWriter)
- description and source-code
```javascript
function BufferWriter() {
    Writer.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferWriter.alloc"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferWriter.</span>alloc (size)](#apidoc.element.protobufjs.BufferWriter.alloc)
- description and source-code
```javascript
function alloc_buffer(size) {
    return (BufferWriter.alloc = util._Buffer_allocUnsafe)(size);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.BufferWriter.prototype"></a>[module protobufjs.BufferWriter.prototype](#apidoc.module.protobufjs.BufferWriter.prototype)

#### <a name="apidoc.element.protobufjs.BufferWriter.prototype.bytes"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>bytes (value)](#apidoc.element.protobufjs.BufferWriter.prototype.bytes)
- description and source-code
```javascript
function write_bytes_buffer(value) {
    if (util.isString(value))
        value = util._Buffer_from(value, "base64");
    var len = value.length >>> 0;
    this.uint32(len);
    if (len)
        this.push(writeBytesBuffer, len, value);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferWriter.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>constructor ()](#apidoc.element.protobufjs.BufferWriter.prototype.constructor)
- description and source-code
```javascript
function BufferWriter() {
    Writer.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.BufferWriter.prototype.string"></a>[function <span class="apidocSignatureSpan">protobufjs.BufferWriter.prototype.</span>string (value)](#apidoc.element.protobufjs.BufferWriter.prototype.string)
- description and source-code
```javascript
function write_string_buffer(value) {
    var len = Buffer.byteLength(value);
    this.uint32(len);
    if (len)
        this.push(writeStringBuffer, len, value);
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Class"></a>[module protobufjs.Class](#apidoc.module.protobufjs.Class)

#### <a name="apidoc.element.protobufjs.Class.Class"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Class (type, ctor)](#apidoc.element.protobufjs.Class.Class)
- description and source-code
```javascript
function Class(type, ctor) {
    if (!Type)
        Type = require("./type");

    if (!(type instanceof Type))
        throw TypeError("type must be a Type");

    if (ctor) {
        if (typeof ctor !== "function")
            throw TypeError("ctor must be a function");
    } else
        ctor = Class.generate(type).eof(type.name); // named constructor function (codegen is required anyway)

    // Let's pretend...
    ctor.constructor = Class;

    // new Class() -> Message.prototype
    (ctor.prototype = new Message()).constructor = ctor;

    // Static methods on Message are instance methods on Class and vice versa
    util.merge(ctor, Message, true);

    // Classes and messages reference their reflected type
    ctor.$type = type;
    ctor.prototype.$type = type;

    // Messages have non-enumerable default values on their prototype
    var i = 0;
    for (; i < /* initializes */ type.fieldsArray.length; ++i) {
        // objects on the prototype must be immmutable. users must assign a new object instance and
        // cannot use Array#push on empty arrays on the prototype for example, as this would modify
        // the value on the prototype for ALL messages of this type. Hence, these objects are frozen.
        ctor.prototype[type._fieldsArray[i].name] = Array.isArray(type._fieldsArray[i].resolve().defaultValue)
            ? util.emptyArray
            : util.isObject(type._fieldsArray[i].defaultValue) && !type._fieldsArray[i].long
              ? util.emptyObject
              : type._fieldsArray[i].defaultValue; // if a long, it is frozen when initialized
    }

    // Messages have non-enumerable getters and setters for each virtual oneof field
    var ctorProperties = {};
    for (i = 0; i < /* initializes */ type.oneofsArray.length; ++i)
        ctorProperties[type._oneofsArray[i].resolve().name] = {
            get: util.oneOfGetter(type._oneofsArray[i].oneof),
            set: util.oneOfSetter(type._oneofsArray[i].oneof)
        };
    if (i)
        Object.defineProperties(ctor.prototype, ctorProperties);

    // Register
    type.ctor = ctor;

    return ctor.prototype;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Class.create"></a>[function <span class="apidocSignatureSpan">protobufjs.Class.</span>create (type, ctor)](#apidoc.element.protobufjs.Class.create)
- description and source-code
```javascript
function Class(type, ctor) {
    if (!Type)
        Type = require("./type");

    if (!(type instanceof Type))
        throw TypeError("type must be a Type");

    if (ctor) {
        if (typeof ctor !== "function")
            throw TypeError("ctor must be a function");
    } else
        ctor = Class.generate(type).eof(type.name); // named constructor function (codegen is required anyway)

    // Let's pretend...
    ctor.constructor = Class;

    // new Class() -> Message.prototype
    (ctor.prototype = new Message()).constructor = ctor;

    // Static methods on Message are instance methods on Class and vice versa
    util.merge(ctor, Message, true);

    // Classes and messages reference their reflected type
    ctor.$type = type;
    ctor.prototype.$type = type;

    // Messages have non-enumerable default values on their prototype
    var i = 0;
    for (; i < /* initializes */ type.fieldsArray.length; ++i) {
        // objects on the prototype must be immmutable. users must assign a new object instance and
        // cannot use Array#push on empty arrays on the prototype for example, as this would modify
        // the value on the prototype for ALL messages of this type. Hence, these objects are frozen.
        ctor.prototype[type._fieldsArray[i].name] = Array.isArray(type._fieldsArray[i].resolve().defaultValue)
            ? util.emptyArray
            : util.isObject(type._fieldsArray[i].defaultValue) && !type._fieldsArray[i].long
              ? util.emptyObject
              : type._fieldsArray[i].defaultValue; // if a long, it is frozen when initialized
    }

    // Messages have non-enumerable getters and setters for each virtual oneof field
    var ctorProperties = {};
    for (i = 0; i < /* initializes */ type.oneofsArray.length; ++i)
        ctorProperties[type._oneofsArray[i].resolve().name] = {
            get: util.oneOfGetter(type._oneofsArray[i].oneof),
            set: util.oneOfSetter(type._oneofsArray[i].oneof)
        };
    if (i)
        Object.defineProperties(ctor.prototype, ctorProperties);

    // Register
    type.ctor = ctor;

    return ctor.prototype;
}
```
- example usage
```shell
...
* **Message.decodeDelimited**(reader: 'Reader|Uint8Array'): 'Message'<br />
works like 'Message.decode' but additionally reads the length of the message prepended as a varint.

* **Message.create**(properties: 'Object'): 'Message'<br />
quickly creates a new runtime message from known to be valid properties without any conversion being performed. Where applicable
, it is recommended to prefer 'Message.create' over 'Message.fromObject'.

'''js
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
...
```

#### <a name="apidoc.element.protobufjs.Class.generate"></a>[function <span class="apidocSignatureSpan">protobufjs.Class.</span>generate (type)](#apidoc.element.protobufjs.Class.generate)
- description and source-code
```javascript
function generate(type) { // eslint-disable-line no-unused-vars
    /* eslint-disable no-unexpected-multiline */
    var gen = util.codegen("p");
    // explicitly initialize mutable object/array fields so that these aren't just inherited from the prototype
    for (var i = 0, field; i < type.fieldsArray.length; ++i)
        if ((field = type._fieldsArray[i]).map) gen
            ("this%s={}", util.safeProp(field.name));
        else if (field.repeated) gen
            ("this%s=[]", util.safeProp(field.name));
    return gen
    ("if(p){")
        ("for(var ks=Object.keys(p),i=0;i<ks.length;++i)")
            ("this[ks[i]]=p[ks[i]];")
    ("}");
    /* eslint-enable no-unexpected-multiline */
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Enum"></a>[module protobufjs.Enum](#apidoc.module.protobufjs.Enum)

#### <a name="apidoc.element.protobufjs.Enum.Enum"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Enum (name, values, options)](#apidoc.element.protobufjs.Enum.Enum)
- description and source-code
```javascript
function Enum(name, values, options) {
    ReflectionObject.call(this, name, options);

    if (values && typeof values !== "object")
        throw TypeError("values must be an object");

    /**
     * Enum values by id.
     * @type {Object.<number,string>}
     */
    this.valuesById = {};

    /**
     * Enum values by name.
     * @type {Object.<string,number>}
     */
    this.values = Object.create(this.valuesById); // toJSON, marker

    /**
     * Value comment texts, if any.
     * @type {Object.<string,string>}
     */
    this.comments = {};

    // Note that values inherit valuesById on their prototype which makes them a TypeScript-
    // compatible enum. This is used by pbts to write actual enum definitions that work for
    // static and reflection code alike instead of emitting generic object definitions.

    if (values)
        for (var keys = Object.keys(values), i = 0; i < keys.length; ++i)
            this.valuesById[ this.values[keys[i]] = values[keys[i]] ] = keys[i];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Enum.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Enum.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Enum.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new Enum(name, json.values, json.options);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Enum.prototype"></a>[module protobufjs.Enum.prototype](#apidoc.module.protobufjs.Enum.prototype)

#### <a name="apidoc.element.protobufjs.Enum.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>add (name, id, comment)](#apidoc.element.protobufjs.Enum.prototype.add)
- description and source-code
```javascript
add = function (name, id, comment) {
    // utilized by the parser but not by .fromJSON

    if (!util.isString(name))
        throw TypeError("name must be a string");

    if (!util.isInteger(id))
        throw TypeError("id must be an integer");

    if (this.values[name] !== undefined)
        throw Error("duplicate name");

    if (this.valuesById[id] !== undefined) {
        if (!(this.options && this.options.allow_alias))
            throw Error("duplicate id");
        this.values[name] = id;
    } else
        this.valuesById[this.values[name] = id] = name;

    this.comments[name] = comment || null;
    return this;
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.Enum.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>constructor (name, values, options)](#apidoc.element.protobufjs.Enum.prototype.constructor)
- description and source-code
```javascript
function Enum(name, values, options) {
    ReflectionObject.call(this, name, options);

    if (values && typeof values !== "object")
        throw TypeError("values must be an object");

    /**
     * Enum values by id.
     * @type {Object.<number,string>}
     */
    this.valuesById = {};

    /**
     * Enum values by name.
     * @type {Object.<string,number>}
     */
    this.values = Object.create(this.valuesById); // toJSON, marker

    /**
     * Value comment texts, if any.
     * @type {Object.<string,string>}
     */
    this.comments = {};

    // Note that values inherit valuesById on their prototype which makes them a TypeScript-
    // compatible enum. This is used by pbts to write actual enum definitions that work for
    // static and reflection code alike instead of emitting generic object definitions.

    if (values)
        for (var keys = Object.keys(values), i = 0; i < keys.length; ++i)
            this.valuesById[ this.values[keys[i]] = values[keys[i]] ] = keys[i];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Enum.prototype.remove"></a>[function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>remove (name)](#apidoc.element.protobufjs.Enum.prototype.remove)
- description and source-code
```javascript
remove = function (name) {

    if (!util.isString(name))
        throw TypeError("name must be a string");

    var val = this.values[name];
    if (val === undefined)
        throw Error("name does not exist");

    delete this.valuesById[val];
    delete this.values[name];
    delete this.comments[name];

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Enum.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Enum.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Enum.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        options : this.options,
        values  : this.values
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Field"></a>[module protobufjs.Field](#apidoc.module.protobufjs.Field)

#### <a name="apidoc.element.protobufjs.Field.Field"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Field (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field.Field)
- description and source-code
```javascript
function Field(name, id, type, rule, extend, options) {

    if (util.isObject(rule)) {
        options = rule;
        rule = extend = undefined;
    } else if (util.isObject(extend)) {
        options = extend;
        extend = undefined;
    }

    ReflectionObject.call(this, name, options);

    if (!util.isInteger(id) || id < 0)
        throw TypeError("id must be a non-negative integer");

    if (!util.isString(type))
        throw TypeError("type must be a string");

    if (rule !== undefined && !ruleRe.test(rule = rule.toString().toLowerCase()))
        throw TypeError("rule must be a string rule");

    if (extend !== undefined && !util.isString(extend))
        throw TypeError("extend must be a string");

    /**
     * Field rule, if any.
     * @type {string|undefined}
     */
    this.rule = rule && rule !== "optional" ? rule : undefined; // toJSON

    /**
     * Field type.
     * @type {string}
     */
    this.type = type; // toJSON

    /**
     * Unique field id.
     * @type {number}
     */
    this.id = id; // toJSON, marker

    /**
     * Extended type if different from parent.
     * @type {string|undefined}
     */
    this.extend = extend || undefined; // toJSON

    /**
     * Whether this field is required.
     * @type {boolean}
     */
    this.required = rule === "required";

    /**
     * Whether this field is optional.
     * @type {boolean}
     */
    this.optional = !this.required;

    /**
     * Whether this field is repeated.
     * @type {boolean}
     */
    this.repeated = rule === "repeated";

    /**
     * Whether this field is a map or not.
     * @type {boolean}
     */
    this.map = false;

    /**
     * Message this field belongs to.
     * @type {?Type}
     */
    this.message = null;

    /**
     * OneOf this field belongs to, if any,
     * @type {?OneOf}
     */
    this.partOf = null;

    /**
     * The field type's default value.
     * @type {*}
     */
    this.typeDefault = null;

    /**
     * The field's default value on prototypes.
     * @type {*}
     */
    this.defaultValue = null;

    /**
     * Whether this field's value should be treated as a long.
     * @type {boolean}
     */
    this.long = util.Long ? types.long[type] !== undefined : /* istanbul ignore next */ false;

    /**
     * Whether this field's value is a buffer.
     * @type {boolean}
     */
    this.bytes = type === "bytes";

    /**
     * Resolved type if not a basic type.
     * @type {?(Type|Enum)}
     */
    this.resolvedType = null;

    /**
     * Sister-field within the extended type if a declaring extension field.
     * @type {?Field}
     */
    this.extensionField = null;

    /**
     * Sister-field within the declaring namespace if an extended field.
     * @type {?Field}
     */
    this.declaringField = null;

    /**
     * Internally remembers whether this field is packed.
     * @type {?boolean}
     * @private
     */
    this._packed = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Field.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Field.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Field.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new Field(name, json.id, json.type, json.rule, json.extend, json.options);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Field.prototype"></a>[module protobufjs.Field.prototype](#apidoc.module.protobufjs.Field.prototype)

#### <a name="apidoc.element.protobufjs.Field.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>constructor (name, id, type, rule, extend, options)](#apidoc.element.protobufjs.Field.prototype.constructor)
- description and source-code
```javascript
function Field(name, id, type, rule, extend, options) {

    if (util.isObject(rule)) {
        options = rule;
        rule = extend = undefined;
    } else if (util.isObject(extend)) {
        options = extend;
        extend = undefined;
    }

    ReflectionObject.call(this, name, options);

    if (!util.isInteger(id) || id < 0)
        throw TypeError("id must be a non-negative integer");

    if (!util.isString(type))
        throw TypeError("type must be a string");

    if (rule !== undefined && !ruleRe.test(rule = rule.toString().toLowerCase()))
        throw TypeError("rule must be a string rule");

    if (extend !== undefined && !util.isString(extend))
        throw TypeError("extend must be a string");

    /**
     * Field rule, if any.
     * @type {string|undefined}
     */
    this.rule = rule && rule !== "optional" ? rule : undefined; // toJSON

    /**
     * Field type.
     * @type {string}
     */
    this.type = type; // toJSON

    /**
     * Unique field id.
     * @type {number}
     */
    this.id = id; // toJSON, marker

    /**
     * Extended type if different from parent.
     * @type {string|undefined}
     */
    this.extend = extend || undefined; // toJSON

    /**
     * Whether this field is required.
     * @type {boolean}
     */
    this.required = rule === "required";

    /**
     * Whether this field is optional.
     * @type {boolean}
     */
    this.optional = !this.required;

    /**
     * Whether this field is repeated.
     * @type {boolean}
     */
    this.repeated = rule === "repeated";

    /**
     * Whether this field is a map or not.
     * @type {boolean}
     */
    this.map = false;

    /**
     * Message this field belongs to.
     * @type {?Type}
     */
    this.message = null;

    /**
     * OneOf this field belongs to, if any,
     * @type {?OneOf}
     */
    this.partOf = null;

    /**
     * The field type's default value.
     * @type {*}
     */
    this.typeDefault = null;

    /**
     * The field's default value on prototypes.
     * @type {*}
     */
    this.defaultValue = null;

    /**
     * Whether this field's value should be treated as a long.
     * @type {boolean}
     */
    this.long = util.Long ? types.long[type] !== undefined : /* istanbul ignore next */ false;

    /**
     * Whether this field's value is a buffer.
     * @type {boolean}
     */
    this.bytes = type === "bytes";

    /**
     * Resolved type if not a basic type.
     * @type {?(Type|Enum)}
     */
    this.resolvedType = null;

    /**
     * Sister-field within the extended type if a declaring extension field.
     * @type {?Field}
     */
    this.extensionField = null;

    /**
     * Sister-field within the declaring namespace if an extended field.
     * @type {?Field}
     */
    this.declaringField = null;

    /**
     * Internally remembers whether this field is packed.
     * @type {?boolean}
     * @private
     */
    this._packed = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Field.prototype.resolve"></a>[function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>resolve ()](#apidoc.element.protobufjs.Field.prototype.resolve)
- description and source-code
```javascript
function resolve() {

    if (this.resolved)
        return this;

    if ((this.typeDefault = types.defaults[this.type]) === undefined) { // if not a basic type, resolve it

        /* istanbul ignore if */
        if (!Type)
            Type = require("./type");

        this.resolvedType = (this.declaringField ? this.declaringField.parent : this.parent).lookupTypeOrEnum(this.type);
        if (this.resolvedType instanceof Type)
            this.typeDefault = null;
        else // instanceof Enum
            this.typeDefault = this.resolvedType.values[Object.keys(this.resolvedType.values)[0]]; // first defined
    }

    // use explicitly set default value if present
    if (this.options && this.options["default"] !== undefined) {
        this.typeDefault = this.options["default"];
        if (this.resolvedType instanceof Enum && typeof this.typeDefault === "string")
            this.typeDefault = this.resolvedType.values[this.typeDefault];
    }

    // remove unnecessary packed option (parser adds this) if not referencing an enum
    if (this.options && this.options.packed !== undefined && this.resolvedType && !(this.resolvedType instanceof Enum))
        delete this.options.packed;

    // convert to internal data type if necesssary
    if (this.long) {
        this.typeDefault = util.Long.fromNumber(this.typeDefault, this.type.charAt(0) === "u");

        /* istanbul ignore else */
        if (Object.freeze)
            Object.freeze(this.typeDefault); // long instances are meant to be immutable anyway (i.e. use small int cache that even
 requires it)

    } else if (this.bytes && typeof this.typeDefault === "string") {
        var buf;
        if (util.base64.test(this.typeDefault))
            util.base64.decode(this.typeDefault, buf = util.newBuffer(util.base64.length(this.typeDefault)), 0);
        else
            util.utf8.write(this.typeDefault, buf = util.newBuffer(util.utf8.length(this.typeDefault)), 0);
        this.typeDefault = buf;
    }

    // take special care of maps and repeated fields
    if (this.map)
        this.defaultValue = util.emptyObject;
    else if (this.repeated)
        this.defaultValue = util.emptyArray;
    else
        this.defaultValue = this.typeDefault;

    return ReflectionObject.prototype.resolve.call(this);
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Field.prototype.setOption"></a>[function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>setOption (name, value, ifNotSet)](#apidoc.element.protobufjs.Field.prototype.setOption)
- description and source-code
```javascript
function setOption(name, value, ifNotSet) {
    if (name === "packed") // clear cached before setting
        this._packed = null;
    return ReflectionObject.prototype.setOption.call(this, name, value, ifNotSet);
}
```
- example usage
```shell
...
parent.add(field);

// JSON defaults to packed=true if not set so we have to set packed=false explicity when
// parsing proto2 descriptors without the option, where applicable. This must be done for
// any type (not just packable types) because enums also use varint encoding and it is not
// yet known whether a type is an enum or not.
if (!isProto3 && field.repeated)
    field.setOption("packed", false, /* ifNotSet */ true);
    }

    function parseGroup(parent, rule) {
var name = next();

/* istanbul ignore if */
if (!nameRe.test(name))
...
```

#### <a name="apidoc.element.protobufjs.Field.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Field.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Field.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        rule    : this.rule !== "optional" && this.rule || undefined,
        type    : this.type,
        id      : this.id,
        extend  : this.extend,
        options : this.options
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.MapField"></a>[module protobufjs.MapField](#apidoc.module.protobufjs.MapField)

#### <a name="apidoc.element.protobufjs.MapField.MapField"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>MapField (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField.MapField)
- description and source-code
```javascript
function MapField(name, id, keyType, type, options) {
    Field.call(this, name, id, type, options);

    /* istanbul ignore if */
    if (!util.isString(keyType))
        throw TypeError("keyType must be a string");

    /**
     * Key type.
     * @type {string}
     */
    this.keyType = keyType; // toJSON, marker

    /**
     * Resolved key type if not a basic type.
     * @type {?ReflectionObject}
     */
    this.resolvedKeyType = null;

    // Overrides Field#map
    this.map = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.MapField.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.MapField.</span>fromJSON (name, json)](#apidoc.element.protobufjs.MapField.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new MapField(name, json.id, json.keyType, json.type, json.options);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.MapField.prototype"></a>[module protobufjs.MapField.prototype](#apidoc.module.protobufjs.MapField.prototype)

#### <a name="apidoc.element.protobufjs.MapField.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>constructor (name, id, keyType, type, options)](#apidoc.element.protobufjs.MapField.prototype.constructor)
- description and source-code
```javascript
function MapField(name, id, keyType, type, options) {
    Field.call(this, name, id, type, options);

    /* istanbul ignore if */
    if (!util.isString(keyType))
        throw TypeError("keyType must be a string");

    /**
     * Key type.
     * @type {string}
     */
    this.keyType = keyType; // toJSON, marker

    /**
     * Resolved key type if not a basic type.
     * @type {?ReflectionObject}
     */
    this.resolvedKeyType = null;

    // Overrides Field#map
    this.map = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.MapField.prototype.resolve"></a>[function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>resolve ()](#apidoc.element.protobufjs.MapField.prototype.resolve)
- description and source-code
```javascript
function resolve() {
    if (this.resolved)
        return this;

    // Besides a value type, map fields have a key type that may be "any scalar type except for floating point types and bytes"
    if (types.mapKey[this.keyType] === undefined)
        throw Error("invalid key type: " + this.keyType);

    return Field.prototype.resolve.call(this);
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.MapField.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.MapField.prototype.</span>toJSON ()](#apidoc.element.protobufjs.MapField.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        keyType : this.keyType,
        type    : this.type,
        id      : this.id,
        extend  : this.extend,
        options : this.options
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Message"></a>[module protobufjs.Message](#apidoc.module.protobufjs.Message)

#### <a name="apidoc.element.protobufjs.Message.Message"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Message (properties)](#apidoc.element.protobufjs.Message.Message)
- description and source-code
```javascript
function Message(properties) {
    // not used internally
    if (properties)
        for (var keys = Object.keys(properties), i = 0; i < keys.length; ++i)
            this[keys[i]] = properties[keys[i]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message.decode"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>decode (reader)](#apidoc.element.protobufjs.Message.decode)
- description and source-code
```javascript
function decode(reader) {
    return this.$type.decode(reader);
}
```
- example usage
```shell
...
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.

'''js
try {
  var decodedMessage = AwesomeMessage.decode(buffer);
} catch (e) {
    if (e instanceof protobuf.util.ProtocolError) {
      // e.instance holds the so far decoded message with missing required fields
    } else {
      // wire format is invalid
    }
}
...
```

#### <a name="apidoc.element.protobufjs.Message.decodeDelimited"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>decodeDelimited (reader)](#apidoc.element.protobufjs.Message.decodeDelimited)
- description and source-code
```javascript
function decodeDelimited(reader) {
    return this.$type.decodeDelimited(reader);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message.encode"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>encode (message, writer)](#apidoc.element.protobufjs.Message.encode)
- description and source-code
```javascript
function encode(message, writer) {
    return this.$type.encode(message, writer);
}
```
- example usage
```shell
...
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.

'''js
var buffer = AwesomeMessage.encode(message).finish();
'''

* **Message.encodeDelimited**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.
...
```

#### <a name="apidoc.element.protobufjs.Message.encodeDelimited"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>encodeDelimited (message, writer)](#apidoc.element.protobufjs.Message.encodeDelimited)
- description and source-code
```javascript
function encodeDelimited(message, writer) {
    return this.$type.encodeDelimited(message, writer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message.from"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>from (object)](#apidoc.element.protobufjs.Message.from)
- description and source-code
```javascript
function fromObject(object) {
    return this.$type.fromObject(object);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message.fromObject"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>fromObject (object)](#apidoc.element.protobufjs.Message.fromObject)
- description and source-code
```javascript
function fromObject(object) {
    return this.$type.fromObject(object);
}
```
- example usage
```shell
...
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
...
```

#### <a name="apidoc.element.protobufjs.Message.toObject"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>toObject (message, options)](#apidoc.element.protobufjs.Message.toObject)
- description and source-code
```javascript
function toObject(message, options) {
    return this.$type.toObject(message, options);
}
```
- example usage
```shell
...
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
var object = AwesomeMessage.toObject(message, {
  enums: String,  // enums as string names
  longs: String,  // longs as strings (requires long.js)
  bytes: String,  // bytes as base64 encoded strings
  defaults: true, // includes default values
  arrays: true,   // populates empty arrays (repeated fields) even if defaults=false
  objects: true,  // populates empty objects (map fields) even if defaults=false
  oneofs: true    // includes virtual oneof fields set to the present field's name
...
```

#### <a name="apidoc.element.protobufjs.Message.verify"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.</span>verify (message)](#apidoc.element.protobufjs.Message.verify)
- description and source-code
```javascript
function verify(message) {
    return this.$type.verify(message);
}
```
- example usage
```shell
...
Note that **Message** below refers to any message type. See the next section for the definition of a [valid message](#valid-message
).

* **Message.verify**(message: 'Object'): 'null|string'<br />
explicitly performs verification prior to encoding a plain object. Instead of throwing, it returns the error message as a string
, if any.

'''js
var payload = "invalid (not an object)";
var err = AwesomeMessage.verify(payload);
if (err)
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.
...
```



# <a name="apidoc.module.protobufjs.Message.prototype"></a>[module protobufjs.Message.prototype](#apidoc.module.protobufjs.Message.prototype)

#### <a name="apidoc.element.protobufjs.Message.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Message.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return this.$type.toObject(this, util.toJSONOptions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Message.prototype.toObject"></a>[function <span class="apidocSignatureSpan">protobufjs.Message.prototype.</span>toObject (options)](#apidoc.element.protobufjs.Message.prototype.toObject)
- description and source-code
```javascript
function toObject(options) {
    return this.$type.toObject(this, options);
}
```
- example usage
```shell
...
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
var object = AwesomeMessage.toObject(message, {
  enums: String,  // enums as string names
  longs: String,  // longs as strings (requires long.js)
  bytes: String,  // bytes as base64 encoded strings
  defaults: true, // includes default values
  arrays: true,   // populates empty arrays (repeated fields) even if defaults=false
  objects: true,  // populates empty objects (map fields) even if defaults=false
  oneofs: true    // includes virtual oneof fields set to the present field's name
...
```



# <a name="apidoc.module.protobufjs.Method"></a>[module protobufjs.Method](#apidoc.module.protobufjs.Method)

#### <a name="apidoc.element.protobufjs.Method.Method"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Method (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method.Method)
- description and source-code
```javascript
function Method(name, type, requestType, responseType, requestStream, responseStream, options) {

    /* istanbul ignore next */
    if (util.isObject(requestStream)) {
        options = requestStream;
        requestStream = responseStream = undefined;
    } else if (util.isObject(responseStream)) {
        options = responseStream;
        responseStream = undefined;
    }

    /* istanbul ignore if */
    if (!(type === undefined || util.isString(type)))
        throw TypeError("type must be a string");

    /* istanbul ignore if */
    if (!util.isString(requestType))
        throw TypeError("requestType must be a string");

    /* istanbul ignore if */
    if (!util.isString(responseType))
        throw TypeError("responseType must be a string");

    ReflectionObject.call(this, name, options);

    /**
     * Method type.
     * @type {string}
     */
    this.type = type || "rpc"; // toJSON

    /**
     * Request type.
     * @type {string}
     */
    this.requestType = requestType; // toJSON, marker

    /**
     * Whether requests are streamed or not.
     * @type {boolean|undefined}
     */
    this.requestStream = requestStream ? true : undefined; // toJSON

    /**
     * Response type.
     * @type {string}
     */
    this.responseType = responseType; // toJSON

    /**
     * Whether responses are streamed or not.
     * @type {boolean|undefined}
     */
    this.responseStream = responseStream ? true : undefined; // toJSON

    /**
     * Resolved request type.
     * @type {?Type}
     */
    this.resolvedRequestType = null;

    /**
     * Resolved response type.
     * @type {?Type}
     */
    this.resolvedResponseType = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Method.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Method.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Method.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new Method(name, json.type, json.requestType, json.responseType, json.requestStream, json.responseStream, json.options
);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Method.prototype"></a>[module protobufjs.Method.prototype](#apidoc.module.protobufjs.Method.prototype)

#### <a name="apidoc.element.protobufjs.Method.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>constructor (name, type, requestType, responseType, requestStream, responseStream, options)](#apidoc.element.protobufjs.Method.prototype.constructor)
- description and source-code
```javascript
function Method(name, type, requestType, responseType, requestStream, responseStream, options) {

    /* istanbul ignore next */
    if (util.isObject(requestStream)) {
        options = requestStream;
        requestStream = responseStream = undefined;
    } else if (util.isObject(responseStream)) {
        options = responseStream;
        responseStream = undefined;
    }

    /* istanbul ignore if */
    if (!(type === undefined || util.isString(type)))
        throw TypeError("type must be a string");

    /* istanbul ignore if */
    if (!util.isString(requestType))
        throw TypeError("requestType must be a string");

    /* istanbul ignore if */
    if (!util.isString(responseType))
        throw TypeError("responseType must be a string");

    ReflectionObject.call(this, name, options);

    /**
     * Method type.
     * @type {string}
     */
    this.type = type || "rpc"; // toJSON

    /**
     * Request type.
     * @type {string}
     */
    this.requestType = requestType; // toJSON, marker

    /**
     * Whether requests are streamed or not.
     * @type {boolean|undefined}
     */
    this.requestStream = requestStream ? true : undefined; // toJSON

    /**
     * Response type.
     * @type {string}
     */
    this.responseType = responseType; // toJSON

    /**
     * Whether responses are streamed or not.
     * @type {boolean|undefined}
     */
    this.responseStream = responseStream ? true : undefined; // toJSON

    /**
     * Resolved request type.
     * @type {?Type}
     */
    this.resolvedRequestType = null;

    /**
     * Resolved response type.
     * @type {?Type}
     */
    this.resolvedResponseType = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Method.prototype.resolve"></a>[function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>resolve ()](#apidoc.element.protobufjs.Method.prototype.resolve)
- description and source-code
```javascript
function resolve() {

    /* istanbul ignore if */
    if (this.resolved)
        return this;

    this.resolvedRequestType = this.parent.lookupType(this.requestType);
    this.resolvedResponseType = this.parent.lookupType(this.responseType);

    return ReflectionObject.prototype.resolve.call(this);
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Method.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Method.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Method.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        type           : this.type !== "rpc" && /* istanbul ignore next */ this.type || undefined,
        requestType    : this.requestType,
        requestStream  : this.requestStream,
        responseType   : this.responseType,
        responseStream : this.responseStream,
        options        : this.options
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Namespace"></a>[module protobufjs.Namespace](#apidoc.module.protobufjs.Namespace)

#### <a name="apidoc.element.protobufjs.Namespace.Namespace"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Namespace (name, options)](#apidoc.element.protobufjs.Namespace.Namespace)
- description and source-code
```javascript
function Namespace(name, options) {
    ReflectionObject.call(this, name, options);

    /**
     * Nested objects by name.
     * @type {Object.<string,ReflectionObject>|undefined}
     */
    this.nested = undefined; // toJSON

    /**
     * Cached nested objects as an array.
     * @type {?ReflectionObject[]}
     * @private
     */
    this._nestedArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>_configure (Type_, Service_)](#apidoc.element.protobufjs.Namespace._configure)
- description and source-code
```javascript
_configure = function (Type_, Service_) {
    Type    = Type_;
    Service = Service_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.arrayToJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>arrayToJSON (array)](#apidoc.element.protobufjs.Namespace.arrayToJSON)
- description and source-code
```javascript
function arrayToJSON(array) {
    if (!(array && array.length))
        return undefined;
    var obj = {};
    for (var i = 0; i < array.length; ++i)
        obj[array[i].name] = array[i].toJSON();
    return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Namespace.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new Namespace(name, json.options).addJSON(json.nested);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Namespace.prototype"></a>[module protobufjs.Namespace.prototype](#apidoc.module.protobufjs.Namespace.prototype)

#### <a name="apidoc.element.protobufjs.Namespace.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>add (object)](#apidoc.element.protobufjs.Namespace.prototype.add)
- description and source-code
```javascript
function add(object) {

    if (!(object instanceof Field && object.extend !== undefined || object instanceof Type || object instanceof Enum || object instanceof
 Service || object instanceof Namespace))
        throw TypeError("object must be a valid nested object");

    if (!this.nested)
        this.nested = {};
    else {
        var prev = this.get(object.name);
        if (prev) {
            if (prev instanceof Namespace && object instanceof Namespace && !(prev instanceof Type || prev instanceof Service)) {
                // replace plain namespace but keep existing nested elements and options
                var nested = prev.nestedArray;
                for (var i = 0; i < nested.length; ++i)
                    object.add(nested[i]);
                this.remove(prev);
                if (!this.nested)
                    this.nested = {};
                object.setOptions(prev.options, true);

            } else
                throw Error("duplicate name '" + object.name + "' in " + this);
        }
    }
    this.nested[object.name] = object;
    object.onAdd(this);
    return clearCache(this);
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.addJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>addJSON (nestedJson)](#apidoc.element.protobufjs.Namespace.prototype.addJSON)
- description and source-code
```javascript
function addJSON(nestedJson) {
    var ns = this;
    /* istanbul ignore else */
    if (nestedJson) {
        for (var names = Object.keys(nestedJson), i = 0, nested; i < names.length; ++i) {
            nested = nestedJson[names[i]];
            ns.add( // most to least likely
                ( nested.fields !== undefined
                ? Type.fromJSON
                : nested.values !== undefined
                ? Enum.fromJSON
                : nested.methods !== undefined
                ? Service.fromJSON
                : nested.id !== undefined
                ? Field.fromJSON
                : Namespace.fromJSON )(names[i], nested)
            );
        }
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Namespace.prototype.constructor)
- description and source-code
```javascript
function Namespace(name, options) {
    ReflectionObject.call(this, name, options);

    /**
     * Nested objects by name.
     * @type {Object.<string,ReflectionObject>|undefined}
     */
    this.nested = undefined; // toJSON

    /**
     * Cached nested objects as an array.
     * @type {?ReflectionObject[]}
     * @private
     */
    this._nestedArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.define"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>define (path, json)](#apidoc.element.protobufjs.Namespace.prototype.define)
- description and source-code
```javascript
function define(path, json) {

    if (util.isString(path))
        path = path.split(".");
    else if (!Array.isArray(path))
        throw TypeError("illegal path");
    if (path && path.length && path[0] === "")
        throw Error("path must be relative");

    var ptr = this;
    while (path.length > 0) {
        var part = path.shift();
        if (ptr.nested && ptr.nested[part]) {
            ptr = ptr.nested[part];
            if (!(ptr instanceof Namespace))
                throw Error("path conflicts with non-namespace objects");
        } else
            ptr.add(ptr = new Namespace(part));
    }
    if (json)
        ptr.addJSON(json);
    return ptr;
}
```
- example usage
```shell
...
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''

Detailed information on the reflection structure is available within the [documentation](#documentation).
...
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.get"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>get (name)](#apidoc.element.protobufjs.Namespace.prototype.get)
- description and source-code
```javascript
function get(name) {
    return this.nested && this.nested[name]
        || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.getEnum"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>getEnum (name)](#apidoc.element.protobufjs.Namespace.prototype.getEnum)
- description and source-code
```javascript
function getEnum(name) {
    if (this.nested && this.nested[name] instanceof Enum)
        return this.nested[name].values;
    throw Error("no such enum");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.lookup"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookup (path, filterTypes, parentAlreadyChecked)](#apidoc.element.protobufjs.Namespace.prototype.lookup)
- description and source-code
```javascript
function lookup(path, filterTypes, parentAlreadyChecked) {

    /* istanbul ignore if */
    if (typeof filterTypes === "boolean") {
        parentAlreadyChecked = filterTypes;
        filterTypes = undefined;
    } else if (filterTypes && !Array.isArray(filterTypes))
        filterTypes = [ filterTypes ];

    if (util.isString(path) && path.length) {
        if (path === ".")
            return this.root;
        path = path.split(".");
    } else if (!path.length)
        return this;

    // Start at root if path is absolute
    if (path[0] === "")
        return this.root.lookup(path.slice(1), filterTypes);
    // Test if the first part matches any nested object, and if so, traverse if path contains more
    var found = this.get(path[0]);
    if (found) {
        if (path.length === 1) {
            if (!filterTypes || filterTypes.indexOf(found.constructor) > -1)
                return found;
        } else if (found instanceof Namespace && (found = found.lookup(path.slice(1), filterTypes, true)))
            return found;
    }
    // If there hasn't been a match, try again at the parent
    if (this.parent === null || parentAlreadyChecked)
        return null;
    return this.parent.lookup(path, filterTypes);
}
```
- example usage
```shell
...
message HelloReply {
    string message = 1;
}
'''

'''js
...
var Greeter = root.lookup("Greeter");
var greeter = Greeter.create(/* see above */ rpcImpl, /* request delimited? */ false, /* response delimited? */ false);

greeter.sayHello({ name: 'you' }, function(err, response) {
    console.log('Greeting:', response.message);
});
'''
...
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.lookupEnum"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupEnum (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupEnum)
- description and source-code
```javascript
function lookupEnum(path) {
    var found = this.lookup(path, [ Enum ]);
    if (!found)
        throw Error("no such Enum '" + path + "' in " + this);
    return found;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.lookupService"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupService (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupService)
- description and source-code
```javascript
function lookupService(path) {
    var found = this.lookup(path, [ Service ]);
    if (!found)
        throw Error("no such Service '" + path + "' in " + this);
    return found;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.lookupType"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupType (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupType)
- description and source-code
```javascript
function lookupType(path) {
    var found = this.lookup(path, [ Type ]);
    if (!found)
        throw Error("no such type");
    return found;
}
```
- example usage
```shell
...

'''js
protobuf.load("awesome.proto", function(err, root) {
if (err)
    throw err;

// Obtain a message type
var AwesomeMessage = root.lookupType("awesomepackage.AwesomeMessage");

// Exemplary payload
var payload = { awesomeField: "AwesomeString" };

// Verify the payload if necessary (i.e. when possibly incomplete or invalid)
var errMsg = AwesomeMessage.verify(payload);
if (errMsg)
...
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.lookupTypeOrEnum"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>lookupTypeOrEnum (path)](#apidoc.element.protobufjs.Namespace.prototype.lookupTypeOrEnum)
- description and source-code
```javascript
function lookupTypeOrEnum(path) {
    var found = this.lookup(path, [ Type, Enum ]);
    if (!found)
        throw Error("no such Type or Enum '" + path + "' in " + this);
    return found;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.remove"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>remove (object)](#apidoc.element.protobufjs.Namespace.prototype.remove)
- description and source-code
```javascript
function remove(object) {

    if (!(object instanceof ReflectionObject))
        throw TypeError("object must be a ReflectionObject");
    if (object.parent !== this)
        throw Error(object + " is not a member of " + this);

    delete this.nested[object.name];
    if (!Object.keys(this.nested).length)
        this.nested = undefined;

    object.onRemove(this);
    return clearCache(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.resolveAll"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Namespace.prototype.resolveAll)
- description and source-code
```javascript
function resolveAll() {
    var nested = this.nestedArray, i = 0;
    while (i < nested.length)
        if (nested[i] instanceof Namespace)
            nested[i++].resolveAll();
        else
            nested[i++].resolve();
    return this.resolve();
}
```
- example usage
```shell
...
if (process.argv[2] === "fromjson") {
json = require("../tests/data/test.json");
if (process.argv.indexOf("--resolve") < 0)
    for (var k = 0; k < 10000; ++k)
        protobuf.Root.fromJSON(json);
else
    for (var l = 0; l < 10000; ++l)
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Namespace.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Namespace.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Namespace.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        options : this.options,
        nested  : arrayToJSON(this.nestedArray)
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.OneOf"></a>[module protobufjs.OneOf](#apidoc.module.protobufjs.OneOf)

#### <a name="apidoc.element.protobufjs.OneOf.OneOf"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>OneOf (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf.OneOf)
- description and source-code
```javascript
function OneOf(name, fieldNames, options) {
    if (!Array.isArray(fieldNames)) {
        options = fieldNames;
        fieldNames = undefined;
    }
    ReflectionObject.call(this, name, options);

    /* istanbul ignore if */
    if (!(fieldNames === undefined || Array.isArray(fieldNames)))
        throw TypeError("fieldNames must be an Array");

    /**
     * Field names that belong to this oneof.
     * @type {string[]}
     */
    this.oneof = fieldNames || []; // toJSON, marker

    /**
     * Fields that belong to this oneof as an array for iteration.
     * @type {Field[]}
     * @readonly
     */
    this.fieldsArray = []; // declared readonly for conformance, possibly not yet added to parent
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.</span>fromJSON (name, json)](#apidoc.element.protobufjs.OneOf.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    return new OneOf(name, json.oneof, json.options);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.OneOf.prototype"></a>[module protobufjs.OneOf.prototype](#apidoc.module.protobufjs.OneOf.prototype)

#### <a name="apidoc.element.protobufjs.OneOf.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>add (field)](#apidoc.element.protobufjs.OneOf.prototype.add)
- description and source-code
```javascript
function add(field) {

    /* istanbul ignore if */
    if (!(field instanceof Field))
        throw TypeError("field must be a Field");

    if (field.parent && field.parent !== this.parent)
        field.parent.remove(field);
    this.oneof.push(field.name);
    this.fieldsArray.push(field);
    field.partOf = this; // field.parent remains null
    addFieldsToParent(this);
    return this;
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.OneOf.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>constructor (name, fieldNames, options)](#apidoc.element.protobufjs.OneOf.prototype.constructor)
- description and source-code
```javascript
function OneOf(name, fieldNames, options) {
    if (!Array.isArray(fieldNames)) {
        options = fieldNames;
        fieldNames = undefined;
    }
    ReflectionObject.call(this, name, options);

    /* istanbul ignore if */
    if (!(fieldNames === undefined || Array.isArray(fieldNames)))
        throw TypeError("fieldNames must be an Array");

    /**
     * Field names that belong to this oneof.
     * @type {string[]}
     */
    this.oneof = fieldNames || []; // toJSON, marker

    /**
     * Fields that belong to this oneof as an array for iteration.
     * @type {Field[]}
     * @readonly
     */
    this.fieldsArray = []; // declared readonly for conformance, possibly not yet added to parent
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf.prototype.onAdd"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>onAdd (parent)](#apidoc.element.protobufjs.OneOf.prototype.onAdd)
- description and source-code
```javascript
function onAdd(parent) {
    ReflectionObject.prototype.onAdd.call(this, parent);
    var self = this;
    // Collect present fields
    for (var i = 0; i < this.oneof.length; ++i) {
        var field = parent.get(this.oneof[i]);
        if (field && !field.partOf) {
            field.partOf = self;
            self.fieldsArray.push(field);
        }
    }
    // Add not yet present fields
    addFieldsToParent(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf.prototype.onRemove"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>onRemove (parent)](#apidoc.element.protobufjs.OneOf.prototype.onRemove)
- description and source-code
```javascript
function onRemove(parent) {
    for (var i = 0, field; i < this.fieldsArray.length; ++i)
        if ((field = this.fieldsArray[i]).parent)
            field.parent.remove(field);
    ReflectionObject.prototype.onRemove.call(this, parent);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf.prototype.remove"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>remove (field)](#apidoc.element.protobufjs.OneOf.prototype.remove)
- description and source-code
```javascript
function remove(field) {

    /* istanbul ignore if */
    if (!(field instanceof Field))
        throw TypeError("field must be a Field");

    var index = this.fieldsArray.indexOf(field);

    /* istanbul ignore if */
    if (index < 0)
        throw Error(field + " is not a member of " + this);

    this.fieldsArray.splice(index, 1);
    index = this.oneof.indexOf(field.name);

    /* istanbul ignore else */
    if (index > -1) // theoretical
        this.oneof.splice(index, 1);

    field.partOf = null;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.OneOf.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.OneOf.prototype.</span>toJSON ()](#apidoc.element.protobufjs.OneOf.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    return {
        oneof   : this.oneof,
        options : this.options
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Reader"></a>[module protobufjs.Reader](#apidoc.module.protobufjs.Reader)

#### <a name="apidoc.element.protobufjs.Reader.Reader"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Reader (buffer)](#apidoc.element.protobufjs.Reader.Reader)
- description and source-code
```javascript
function Reader(buffer) {

    /**
     * Read buffer.
     * @type {Uint8Array}
     */
    this.buf = buffer;

    /**
     * Read buffer position.
     * @type {number}
     */
    this.pos = 0;

    /**
     * Read buffer length.
     * @type {number}
     */
    this.len = buffer.length;
}
```
- example usage
```shell
...

if (process.argv.length > 3 && /^\d+$/.test(process.argv[3]))
count = parseInt(process.argv[3], 10);
process.stdout.write(" x " + count + "\n");

function setupBrowser() {
protobuf.Writer.create = function create_browser() { return new protobuf.Writer(); };
protobuf.Reader.create = function create_browser(buf) { return new protobuf.Reader(buf); };
}

switch (process.argv[2]) {
case "encode-browser":
    setupBrowser();
    // eslint-disable-line no-fallthrough
case "encode":
...
```

#### <a name="apidoc.element.protobufjs.Reader._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.</span>_configure (BufferReader_)](#apidoc.element.protobufjs.Reader._configure)
- description and source-code
```javascript
_configure = function (BufferReader_) {
    BufferReader = BufferReader_;

    var fn = util.Long ? "toLong" : /* istanbul ignore next */ "toNumber";
    util.merge(Reader.prototype, {

        int64: function read_int64() {
            return readLongVarint.call(this)[fn](false);
        },

        uint64: function read_uint64() {
            return readLongVarint.call(this)[fn](true);
        },

        sint64: function read_sint64() {
            return readLongVarint.call(this).zzDecode()[fn](false);
        },

        fixed64: function read_fixed64() {
            return readFixed64.call(this)[fn](true);
        },

        sfixed64: function read_sfixed64() {
            return readFixed64.call(this)[fn](false);
        }

    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.create"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.</span>create (buffer)](#apidoc.element.protobufjs.Reader.create)
- description and source-code
```javascript
function create_buffer_setup(buffer) {
    return (Reader.create = function create_buffer(buffer) {
        return util.Buffer.isBuffer(buffer)
            ? new BufferReader(buffer)
            /* istanbul ignore next */
            : create_array(buffer);
    })(buffer);
}
```
- example usage
```shell
...
* **Message.decodeDelimited**(reader: 'Reader|Uint8Array'): 'Message'<br />
works like 'Message.decode' but additionally reads the length of the message prepended as a varint.

* **Message.create**(properties: 'Object'): 'Message'<br />
quickly creates a new runtime message from known to be valid properties without any conversion being performed. Where applicable
, it is recommended to prefer 'Message.create' over 'Message.fromObject'.

'''js
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
...
```



# <a name="apidoc.module.protobufjs.Reader.prototype"></a>[module protobufjs.Reader.prototype](#apidoc.module.protobufjs.Reader.prototype)

#### <a name="apidoc.element.protobufjs.Reader.prototype._slice"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>_slice ()](#apidoc.element.protobufjs.Reader.prototype._slice)
- description and source-code
```javascript
function subarray() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.bool"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>bool ()](#apidoc.element.protobufjs.Reader.prototype.bool)
- description and source-code
```javascript
function read_bool() {
    return this.uint32() !== 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.bytes"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>bytes ()](#apidoc.element.protobufjs.Reader.prototype.bytes)
- description and source-code
```javascript
function read_bytes() {
    var length = this.uint32(),
        start  = this.pos,
        end    = this.pos + length;

    /* istanbul ignore if */
    if (end > this.len)
        throw indexOutOfRange(this, length);

    this.pos += length;
    return start === end // fix for IE 10/Win8 and others' subarray returning array of size 1
        ? new this.buf.constructor(0)
        : this._slice.call(this.buf, start, end);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.double"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>double ()](#apidoc.element.protobufjs.Reader.prototype.double)
- description and source-code
```javascript
function read_double() {

    /* istanbul ignore if */
    if (this.pos + 8 > this.len)
        throw indexOutOfRange(this, 4);

    var value = util.float.readDoubleLE(this.buf, this.pos);
    this.pos += 8;
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.fixed32"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>fixed32 ()](#apidoc.element.protobufjs.Reader.prototype.fixed32)
- description and source-code
```javascript
function read_fixed32() {

    /* istanbul ignore if */
    if (this.pos + 4 > this.len)
        throw indexOutOfRange(this, 4);

    return readFixed32_end(this.buf, this.pos += 4);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.fixed64"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>fixed64 ()](#apidoc.element.protobufjs.Reader.prototype.fixed64)
- description and source-code
```javascript
function read_fixed64() {
    return readFixed64.call(this)[fn](true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.float"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>float ()](#apidoc.element.protobufjs.Reader.prototype.float)
- description and source-code
```javascript
function read_float() {

    /* istanbul ignore if */
    if (this.pos + 4 > this.len)
        throw indexOutOfRange(this, 4);

    var value = util.float.readFloatLE(this.buf, this.pos);
    this.pos += 4;
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.int32"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>int32 ()](#apidoc.element.protobufjs.Reader.prototype.int32)
- description and source-code
```javascript
function read_int32() {
    return this.uint32() | 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.int64"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>int64 ()](#apidoc.element.protobufjs.Reader.prototype.int64)
- description and source-code
```javascript
function read_int64() {
    return readLongVarint.call(this)[fn](false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.sfixed32"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sfixed32 ()](#apidoc.element.protobufjs.Reader.prototype.sfixed32)
- description and source-code
```javascript
function read_sfixed32() {

    /* istanbul ignore if */
    if (this.pos + 4 > this.len)
        throw indexOutOfRange(this, 4);

    return readFixed32_end(this.buf, this.pos += 4) | 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.sfixed64"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sfixed64 ()](#apidoc.element.protobufjs.Reader.prototype.sfixed64)
- description and source-code
```javascript
function read_sfixed64() {
    return readFixed64.call(this)[fn](false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.sint32"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sint32 ()](#apidoc.element.protobufjs.Reader.prototype.sint32)
- description and source-code
```javascript
function read_sint32() {
    var value = this.uint32();
    return value >>> 1 ^ -(value & 1) | 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.sint64"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>sint64 ()](#apidoc.element.protobufjs.Reader.prototype.sint64)
- description and source-code
```javascript
function read_sint64() {
    return readLongVarint.call(this).zzDecode()[fn](false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.skip"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>skip (length)](#apidoc.element.protobufjs.Reader.prototype.skip)
- description and source-code
```javascript
function skip(length) {
    if (typeof length === "number") {
        /* istanbul ignore if */
        if (this.pos + length > this.len)
            throw indexOutOfRange(this, length);
        this.pos += length;
    } else {
        do {
            /* istanbul ignore if */
            if (this.pos >= this.len)
                throw indexOutOfRange(this);
        } while (this.buf[this.pos++] & 128);
    }
    return this;
}
```
- example usage
```shell
...
var field = mtype._fieldsArray[i].resolve(),
    type  = field.resolvedType instanceof Enum ? "uint32" : field.type,
    ref   = "m" + util.safeProp(field.name); gen
    ("case %d:", field.id);

// Map fields
if (field.map) { gen
        ("r.skip().pos++") // assumes id 1 + key wireType
        ("if(%s===util.emptyObject)", ref)
            ("%s={}", ref)
        ("k=r.%s()", field.keyType)
        ("r.pos++"); // assumes id 2 + value wireType
    if (types.long[field.keyType] !== undefined) {
        if (types.basic[type] === undefined) gen
        ("%s[typeof k===\"object\"?util.longToHash(k):k]=types[%d].decode(r,r.uint32())", ref, i); // can't be groups
...
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.skipType"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>skipType (wireType)](#apidoc.element.protobufjs.Reader.prototype.skipType)
- description and source-code
```javascript
skipType = function (wireType) {
    switch (wireType) {
        case 0:
            this.skip();
            break;
        case 1:
            this.skip(8);
            break;
        case 2:
            this.skip(this.uint32());
            break;
        case 3:
            do { // eslint-disable-line no-constant-condition
                if ((wireType = this.uint32() & 7) === 4)
                    break;
                this.skipType(wireType);
            } while (true);
            break;
        case 5:
            this.skip(4);
            break;

        /* istanbul ignore next */
        default:
            throw Error("invalid wire type " + wireType + " at offset " + this.pos);
    }
    return this;
}
```
- example usage
```shell
...
    else gen
            ("%s=r.%s()", ref, type);
    gen
            ("break");
// Unknown fields
} gen
        ("default:")
            ("r.skipType(t&7)")
            ("break")

    ("}")
("}");

// Field presence
for (i = 0; i < mtype._fieldsArray.length; ++i) {
...
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.string"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>string ()](#apidoc.element.protobufjs.Reader.prototype.string)
- description and source-code
```javascript
function read_string() {
    var bytes = this.bytes();
    return utf8.read(bytes, 0, bytes.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.uint32"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>uint32 ()](#apidoc.element.protobufjs.Reader.prototype.uint32)
- description and source-code
```javascript
function read_uint32() {
    value = (         this.buf[this.pos] & 127       ) >>> 0; if (this.buf[this.pos++] < 128) return value;
    value = (value | (this.buf[this.pos] & 127) <<  7) >>> 0; if (this.buf[this.pos++] < 128) return value;
    value = (value | (this.buf[this.pos] & 127) << 14) >>> 0; if (this.buf[this.pos++] < 128) return value;
    value = (value | (this.buf[this.pos] & 127) << 21) >>> 0; if (this.buf[this.pos++] < 128) return value;
    value = (value | (this.buf[this.pos] &  15) << 28) >>> 0; if (this.buf[this.pos++] < 128) return value;

    /* istanbul ignore if */
    if ((this.pos += 5) > this.len) {
        this.pos = this.len;
        throw indexOutOfRange(this, 10);
    }
    return value;
}
```
- example usage
```shell
...
function decoder(mtype) {
/* eslint-disable no-unexpected-multiline */
var gen = util.codegen("r", "l")
("if(!(r instanceof Reader))")
    ("r=Reader.create(r)")
("var c=l===undefined?r.len:r.pos+l,m=new this.ctor" + (mtype.fieldsArray.filter(function(field) { return field.map; }).length ? ",
k" : ""))
("while(r.pos<c){")
    ("var t=r.uint32()");
if (mtype.group) gen
    ("if((t&7)===4)")
        ("break");
gen
    ("switch(t>>>3){");

var i = 0;
...
```

#### <a name="apidoc.element.protobufjs.Reader.prototype.uint64"></a>[function <span class="apidocSignatureSpan">protobufjs.Reader.prototype.</span>uint64 ()](#apidoc.element.protobufjs.Reader.prototype.uint64)
- description and source-code
```javascript
function read_uint64() {
    return readLongVarint.call(this)[fn](true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.ReflectionObject"></a>[module protobufjs.ReflectionObject](#apidoc.module.protobufjs.ReflectionObject)

#### <a name="apidoc.element.protobufjs.ReflectionObject.ReflectionObject"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>ReflectionObject (name, options)](#apidoc.element.protobufjs.ReflectionObject.ReflectionObject)
- description and source-code
```javascript
function ReflectionObject(name, options) {

    if (!util.isString(name))
        throw TypeError("name must be a string");

    if (options && !util.isObject(options))
        throw TypeError("options must be an object");

    /**
     * Options.
     * @type {Object.<string,*>|undefined}
     */
    this.options = options; // toJSON

    /**
     * Unique name within its namespace.
     * @type {string}
     */
    this.name = name;

    /**
     * Parent namespace.
     * @type {?Namespace}
     */
    this.parent = null;

    /**
     * Whether already resolved or not.
     * @type {boolean}
     */
    this.resolved = false;

    /**
     * Comment text, if any.
     * @type {?string}
     */
    this.comment = null;

    /**
     * Defining file name.
     * @type {?string}
     */
    this.filename = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.</span>_configure (Root_)](#apidoc.element.protobufjs.ReflectionObject._configure)
- description and source-code
```javascript
_configure = function (Root_) {
    Root = Root_;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.ReflectionObject.prototype"></a>[module protobufjs.ReflectionObject.prototype](#apidoc.module.protobufjs.ReflectionObject.prototype)

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.getOption"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>getOption (name)](#apidoc.element.protobufjs.ReflectionObject.prototype.getOption)
- description and source-code
```javascript
function getOption(name) {
    if (this.options)
        return this.options[name];
    return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.onAdd"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>onAdd (parent)](#apidoc.element.protobufjs.ReflectionObject.prototype.onAdd)
- description and source-code
```javascript
function onAdd(parent) {
    if (this.parent && this.parent !== parent)
        this.parent.remove(this);
    this.parent = parent;
    this.resolved = false;
    var root = parent.root;
    if (root instanceof Root)
        root._handleAdd(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.onRemove"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>onRemove (parent)](#apidoc.element.protobufjs.ReflectionObject.prototype.onRemove)
- description and source-code
```javascript
function onRemove(parent) {
    var root = parent.root;
    if (root instanceof Root)
        root._handleRemove(this);
    this.parent = null;
    this.resolved = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.resolve"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>resolve ()](#apidoc.element.protobufjs.ReflectionObject.prototype.resolve)
- description and source-code
```javascript
function resolve() {
    if (this.resolved)
        return this;
    if (this.root instanceof Root)
        this.resolved = true; // only if part of a root
    return this;
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.setOption"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>setOption (name, value, ifNotSet)](#apidoc.element.protobufjs.ReflectionObject.prototype.setOption)
- description and source-code
```javascript
function setOption(name, value, ifNotSet) {
    if (!ifNotSet || !this.options || this.options[name] === undefined)
        (this.options || (this.options = {}))[name] = value;
    return this;
}
```
- example usage
```shell
...
parent.add(field);

// JSON defaults to packed=true if not set so we have to set packed=false explicity when
// parsing proto2 descriptors without the option, where applicable. This must be done for
// any type (not just packable types) because enums also use varint encoding and it is not
// yet known whether a type is an enum or not.
if (!isProto3 && field.repeated)
    field.setOption("packed", false, /* ifNotSet */ true);
    }

    function parseGroup(parent, rule) {
var name = next();

/* istanbul ignore if */
if (!nameRe.test(name))
...
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.setOptions"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>setOptions (options, ifNotSet)](#apidoc.element.protobufjs.ReflectionObject.prototype.setOptions)
- description and source-code
```javascript
function setOptions(options, ifNotSet) {
    if (options)
        for (var keys = Object.keys(options), i = 0; i < keys.length; ++i)
            this.setOption(keys[i], options[keys[i]], ifNotSet);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>toJSON ()](#apidoc.element.protobufjs.ReflectionObject.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    throw Error(); // not implemented, shouldn't happen
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.ReflectionObject.prototype.toString"></a>[function <span class="apidocSignatureSpan">protobufjs.ReflectionObject.prototype.</span>toString ()](#apidoc.element.protobufjs.ReflectionObject.prototype.toString)
- description and source-code
```javascript
function toString() {
    var className = this.constructor.className,
        fullName  = this.fullName;
    if (fullName.length)
        return className + " " + fullName;
    return className;
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```



# <a name="apidoc.module.protobufjs.Root"></a>[module protobufjs.Root](#apidoc.module.protobufjs.Root)

#### <a name="apidoc.element.protobufjs.Root.Root"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Root (options)](#apidoc.element.protobufjs.Root.Root)
- description and source-code
```javascript
function Root(options) {
    Namespace.call(this, "", options);

    /**
     * Deferred extension fields.
     * @type {Field[]}
     */
    this.deferred = [];

    /**
     * Resolved file names of loaded files.
     * @type {string[]}
     */
    this.files = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.</span>_configure (Type_, parse_, common_)](#apidoc.element.protobufjs.Root._configure)
- description and source-code
```javascript
_configure = function (Type_, parse_, common_) {
    Type = Type_;
    parse = parse_;
    common = common_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.</span>fromJSON (json, root)](#apidoc.element.protobufjs.Root.fromJSON)
- description and source-code
```javascript
function fromJSON(json, root) {
    if (!root)
        root = new Root();
    if (json.options)
        root.setOptions(json.options);
    return root.addJSON(json.nested);
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Root.prototype"></a>[module protobufjs.Root.prototype](#apidoc.module.protobufjs.Root.prototype)

#### <a name="apidoc.element.protobufjs.Root.prototype._handleAdd"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>_handleAdd (object)](#apidoc.element.protobufjs.Root.prototype._handleAdd)
- description and source-code
```javascript
function _handleAdd(object) {
    if (object instanceof Field) {

        if (/* an extension field (implies not part of a oneof) */ object.extend !== undefined && /* not already handled */ !object
.extensionField)
            if (!tryHandleExtension(this, object))
                this.deferred.push(object);

    } else if (object instanceof Enum) {

        if (exposeRe.test(object.name))
            object.parent[object.name] = object.values; // expose enum values as property of its parent

    } else /* everything else is a namespace */ {

        if (object instanceof Type) // Try to handle any deferred extensions
            for (var i = 0; i < this.deferred.length;)
                if (tryHandleExtension(this, this.deferred[i]))
                    this.deferred.splice(i, 1);
                else
                    ++i;
        for (var j = 0; j < /* initializes */ object.nestedArray.length; ++j) // recurse into the namespace
            this._handleAdd(object._nestedArray[j]);
        if (exposeRe.test(object.name))
            object.parent[object.name] = object; // expose namespace as property of its parent
    }

    // The above also adds uppercased (and thus conflict-free) nested types, services and enums as
    // properties of namespaces just like static code does. This allows using a .d.ts generated for
    // a static module with reflection-based solutions where the condition is met.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root.prototype._handleRemove"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>_handleRemove (object)](#apidoc.element.protobufjs.Root.prototype._handleRemove)
- description and source-code
```javascript
function _handleRemove(object) {
    if (object instanceof Field) {

        if (/* an extension field */ object.extend !== undefined) {
            if (/* already handled */ object.extensionField) { // remove its sister field
                object.extensionField.parent.remove(object.extensionField);
                object.extensionField = null;
            } else { // cancel the extension
                var index = this.deferred.indexOf(object);
                /* istanbul ignore else */
                if (index > -1)
                    this.deferred.splice(index, 1);
            }
        }

    } else if (object instanceof Enum) {

        if (exposeRe.test(object.name))
            delete object.parent[object.name]; // unexpose enum values

    } else if (object instanceof Namespace) {

        for (var i = 0; i < /* initializes */ object.nestedArray.length; ++i) // recurse into the namespace
            this._handleRemove(object._nestedArray[i]);

        if (exposeRe.test(object.name))
            delete object.parent[object.name]; // unexpose namespaces

    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>constructor (options)](#apidoc.element.protobufjs.Root.prototype.constructor)
- description and source-code
```javascript
function Root(options) {
    Namespace.call(this, "", options);

    /**
     * Deferred extension fields.
     * @type {Field[]}
     */
    this.deferred = [];

    /**
     * Resolved file names of loaded files.
     * @type {string[]}
     */
    this.files = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root.prototype.load"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>load (filename, options, callback)](#apidoc.element.protobufjs.Root.prototype.load)
- description and source-code
```javascript
function load(filename, options, callback) {
    if (typeof options === "function") {
        callback = options;
        options = undefined;
    }
    var self = this;
    if (!callback)
        return util.asPromise(load, self, filename, options);

    var sync = callback === SYNC; // undocumented

    // Finishes loading by calling the callback (exactly once)
    function finish(err, root) {
        /* istanbul ignore if */
        if (!callback)
            return;
        var cb = callback;
        callback = null;
        if (sync)
            throw err;
        cb(err, root);
    }

    // Processes a single file
    function process(filename, source) {
        try {
            if (util.isString(source) && source.charAt(0) === "{")
                source = JSON.parse(source);
            if (!util.isString(source))
                self.setOptions(source.options).addJSON(source.nested);
            else {
                parse.filename = filename;
                var parsed = parse(source, self, options),
                    resolved,
                    i = 0;
                if (parsed.imports)
                    for (; i < parsed.imports.length; ++i)
                        if (resolved = self.resolvePath(filename, parsed.imports[i]))
                            fetch(resolved);
                if (parsed.weakImports)
                    for (i = 0; i < parsed.weakImports.length; ++i)
                        if (resolved = self.resolvePath(filename, parsed.weakImports[i]))
                            fetch(resolved, true);
            }
        } catch (err) {
            finish(err);
        }
        if (!sync && !queued)
            finish(null, self); // only once anyway
    }

    // Fetches a single file
    function fetch(filename, weak) {

        // Strip path if this file references a bundled definition
        var idx = filename.lastIndexOf("google/protobuf/");
        if (idx > -1) {
            var altname = filename.substring(idx);
            if (altname in common)
                filename = altname;
        }

        // Skip if already loaded / attempted
        if (self.files.indexOf(filename) > -1)
            return;
        self.files.push(filename);

        // Shortcut bundled definitions
        if (filename in common) {
            if (sync)
                process(filename, common[filename]);
            else {
                ++queued;
                setTimeout(function() {
                    --queued;
                    process(filename, common[filename]);
                });
            }
            return;
        }

        // Otherwise fetch from disk or network
        if (sync) {
            var source;
            try {
                source = util.fs.readFileSync(filename).toString("utf8");
            } catch (err) {
                if (!weak)
                    finish(err);
                return;
            }
            process(filename, source);
        } else {
            ++queued;
            util.fetch(filename, function(err, source) {
                --queued;
                /* istanbul ignore if */
                if (!callback)
                    return; // terminated meanwhile
                if (err) {
                    /* istanbul ignore else */
                    if (!weak)
                        finish(err);
                    else if (!queued) // can't be covered reliably
                        finish(null, self);
                    return;
                }
                process(filename, source);
            });
        }
    }
    var queued = 0;

    // Assembling the root namespace doesn't require working type
    // references anymore, so we can load everything in parallel
    if (util.isString(filename))
        filename = [ filename ];
    for (var i = 0, resolved; i < filename.length; ++i)
        if (resolved = self.resolvePath("", filename[i]))
            fetch(resolved);

    if (sync)
        return self; ...
```
- example usage
```shell
...

message AwesomeMessage {
string awesome_field = 1; // becomes awesomeField
}
'''

'''js
protobuf.load("awesome.proto", function(err, root) {
if (err)
    throw err;

// Obtain a message type
var AwesomeMessage = root.lookupType("awesomepackage.AwesomeMessage");

// Exemplary payload
...
```

#### <a name="apidoc.element.protobufjs.Root.prototype.loadSync"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>loadSync (filename, options)](#apidoc.element.protobufjs.Root.prototype.loadSync)
- description and source-code
```javascript
function loadSync(filename, options) {
    if (!util.isNode)
        throw Error("not supported");
    return this.load(filename, options, SYNC);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Root.prototype.resolveAll"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Root.prototype.resolveAll)
- description and source-code
```javascript
function resolveAll() {
    if (this.deferred.length)
        throw Error("unresolvable extensions: " + this.deferred.map(function(field) {
            return "'extend " + field.extend + "' in " + field.parent.fullName;
        }).join(", "));
    return Namespace.prototype.resolveAll.call(this);
}
```
- example usage
```shell
...
if (process.argv[2] === "fromjson") {
json = require("../tests/data/test.json");
if (process.argv.indexOf("--resolve") < 0)
    for (var k = 0; k < 10000; ++k)
        protobuf.Root.fromJSON(json);
else
    for (var l = 0; l < 10000; ++l)
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Root.prototype.resolvePath"></a>[function <span class="apidocSignatureSpan">protobufjs.Root.prototype.</span>resolvePath (originPath, includePath, alreadyNormalized)](#apidoc.element.protobufjs.Root.prototype.resolvePath)
- description and source-code
```javascript
function resolve(originPath, includePath, alreadyNormalized) {
    if (!alreadyNormalized)
        includePath = normalize(includePath);
    if (isAbsolute(includePath))
        return includePath;
    if (!alreadyNormalized)
        originPath = normalize(originPath);
    return (originPath = originPath.replace(/(?:\/|^)[^/]+$/, "")).length ? normalize(originPath + "/" + includePath) : includePath
;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Service"></a>[module protobufjs.Service](#apidoc.module.protobufjs.Service)

#### <a name="apidoc.element.protobufjs.Service.Service"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Service (name, options)](#apidoc.element.protobufjs.Service.Service)
- description and source-code
```javascript
function Service(name, options) {
    Namespace.call(this, name, options);

    /**
     * Service methods.
     * @type {Object.<string,Method>}
     */
    this.methods = {}; // toJSON, marker

    /**
     * Cached methods as an array.
     * @type {?Method[]}
     * @private
     */
    this._methodsArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Service.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Service.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    var service = new Service(name, json.options);
    /* istanbul ignore else */
    if (json.methods)
        for (var names = Object.keys(json.methods), i = 0; i < names.length; ++i)
            service.add(Method.fromJSON(names[i], json.methods[names[i]]));
    if (json.nested)
        service.addJSON(json.nested);
    return service;
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Service.prototype"></a>[module protobufjs.Service.prototype](#apidoc.module.protobufjs.Service.prototype)

#### <a name="apidoc.element.protobufjs.Service.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>add (object)](#apidoc.element.protobufjs.Service.prototype.add)
- description and source-code
```javascript
function add(object) {

    /* istanbul ignore if */
    if (this.get(object.name))
        throw Error("duplicate name '" + object.name + "' in " + this);

    if (object instanceof Method) {
        this.methods[object.name] = object;
        object.parent = this;
        return clearCache(this);
    }
    return Namespace.prototype.add.call(this, object);
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.Service.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Service.prototype.constructor)
- description and source-code
```javascript
function Service(name, options) {
    Namespace.call(this, name, options);

    /**
     * Service methods.
     * @type {Object.<string,Method>}
     */
    this.methods = {}; // toJSON, marker

    /**
     * Cached methods as an array.
     * @type {?Method[]}
     * @private
     */
    this._methodsArray = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Service.prototype.create"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>create (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.Service.prototype.create)
- description and source-code
```javascript
function create(rpcImpl, requestDelimited, responseDelimited) {
    var rpcService = new rpc.Service(rpcImpl, requestDelimited, responseDelimited);
    for (var i = 0; i < /* initializes */ this.methodsArray.length; ++i) {
        rpcService[util.lcFirst(this._methodsArray[i].resolve().name)] = util.codegen("r","c")("return this.rpcCall(m,q,s,r,c)").
eof(util.lcFirst(this._methodsArray[i].name), {
            m: this._methodsArray[i],
            q: this._methodsArray[i].resolvedRequestType.ctor,
            s: this._methodsArray[i].resolvedResponseType.ctor
        });
    }
    return rpcService;
}
```
- example usage
```shell
...
* **Message.decodeDelimited**(reader: 'Reader|Uint8Array'): 'Message'<br />
works like 'Message.decode' but additionally reads the length of the message prepended as a varint.

* **Message.create**(properties: 'Object'): 'Message'<br />
quickly creates a new runtime message from known to be valid properties without any conversion being performed. Where applicable
, it is recommended to prefer 'Message.create' over 'Message.fromObject'.

'''js
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
...
```

#### <a name="apidoc.element.protobufjs.Service.prototype.get"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>get (name)](#apidoc.element.protobufjs.Service.prototype.get)
- description and source-code
```javascript
function get(name) {
    return this.methods[name]
        || Namespace.prototype.get.call(this, name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Service.prototype.remove"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>remove (object)](#apidoc.element.protobufjs.Service.prototype.remove)
- description and source-code
```javascript
function remove(object) {
    if (object instanceof Method) {

        /* istanbul ignore if */
        if (this.methods[object.name] !== object)
            throw Error(object + " is not a member of " + this);

        delete this.methods[object.name];
        object.parent = null;
        return clearCache(this);
    }
    return Namespace.prototype.remove.call(this, object);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Service.prototype.resolveAll"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Service.prototype.resolveAll)
- description and source-code
```javascript
function resolveAll() {
    var methods = this.methodsArray;
    for (var i = 0; i < methods.length; ++i)
        methods[i].resolve();
    return Namespace.prototype.resolve.call(this);
}
```
- example usage
```shell
...
if (process.argv[2] === "fromjson") {
json = require("../tests/data/test.json");
if (process.argv.indexOf("--resolve") < 0)
    for (var k = 0; k < 10000; ++k)
        protobuf.Root.fromJSON(json);
else
    for (var l = 0; l < 10000; ++l)
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Service.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Service.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Service.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    var inherited = Namespace.prototype.toJSON.call(this);
    return {
        options : inherited && inherited.options || undefined,
        methods : Namespace.arrayToJSON(this.methodsArray) || /* istanbul ignore next */ {},
        nested  : inherited && inherited.nested || undefined
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.Type"></a>[module protobufjs.Type](#apidoc.module.protobufjs.Type)

#### <a name="apidoc.element.protobufjs.Type.Type"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Type (name, options)](#apidoc.element.protobufjs.Type.Type)
- description and source-code
```javascript
function Type(name, options) {
    Namespace.call(this, name, options);

    /**
     * Message fields.
     * @type {Object.<string,Field>}
     */
    this.fields = {};  // toJSON, marker

    /**
     * Oneofs declared within this namespace, if any.
     * @type {Object.<string,OneOf>}
     */
    this.oneofs = undefined; // toJSON

    /**
     * Extension ranges, if any.
     * @type {number[][]}
     */
    this.extensions = undefined; // toJSON

    /**
     * Reserved ranges, if any.
     * @type {Array.<number[]|string>}
     */
    this.reserved = undefined; // toJSON

    /*?
     * Whether this type is a legacy group.
     * @type {boolean|undefined}
     */
    this.group = undefined; // toJSON

    /**
     * Cached fields by id.
     * @type {?Object.<number,Field>}
     * @private
     */
    this._fieldsById = null;

    /**
     * Cached fields as an array.
     * @type {?Field[]}
     * @private
     */
    this._fieldsArray = null;

    /**
     * Cached oneofs as an array.
     * @type {?OneOf[]}
     * @private
     */
    this._oneofsArray = null;

    /**
     * Cached constructor.
     * @type {*}
     * @private
     */
    this._ctor = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.fromJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.</span>fromJSON (name, json)](#apidoc.element.protobufjs.Type.fromJSON)
- description and source-code
```javascript
function fromJSON(name, json) {
    var type = new Type(name, json.options);
    type.extensions = json.extensions;
    type.reserved = json.reserved;
    var names = Object.keys(json.fields),
        i = 0;
    for (; i < names.length; ++i)
        type.add(
            ( typeof json.fields[names[i]].keyType !== "undefined"
            ? MapField.fromJSON
            : Field.fromJSON )(names[i], json.fields[names[i]])
        );
    if (json.oneofs)
        for (names = Object.keys(json.oneofs), i = 0; i < names.length; ++i)
            type.add(OneOf.fromJSON(names[i], json.oneofs[names[i]]));
    if (json.nested)
        for (names = Object.keys(json.nested), i = 0; i < names.length; ++i) {
            var nested = json.nested[names[i]];
            type.add( // most to least likely
                ( nested.id !== undefined
                ? Field.fromJSON
                : nested.fields !== undefined
                ? Type.fromJSON
                : nested.values !== undefined
                ? Enum.fromJSON
                : nested.methods !== undefined
                ? Service.fromJSON
                : Namespace.fromJSON )(names[i], nested)
            );
        }
    if (json.extensions && json.extensions.length)
        type.extensions = json.extensions;
    if (json.reserved && json.reserved.length)
        type.reserved = json.reserved;
    if (json.group)
        type.group = true;
    return type;
}
```
- example usage
```shell
...
| Field              | *ReflectionObject* | rule, **type**, **id**
| MapField           | Field              | **keyType**
| OneOf              | *ReflectionObject* | **oneof** (array of field names)
| Service            | *Namespace*        | **methods**
| Method             | *ReflectionObject* | type, **requestType**, **responseType**, requestStream, responseStream

* **Bold properties** are required. *Italic types* are abstract.
* 'T.fromJSON(name, json)' creates the respective reflection object from a JSON descriptor
* 'T#toJSON()' creates a JSON descriptor from the respective reflection object (its name is used as the key within the parent)

Exclusively using JSON descriptors instead of .proto files enables the use of just the light library (the parser isn't required
in this case).

A JSON descriptor can either be loaded the usual way:

'''js
...
```



# <a name="apidoc.module.protobufjs.Type.prototype"></a>[module protobufjs.Type.prototype](#apidoc.module.protobufjs.Type.prototype)

#### <a name="apidoc.element.protobufjs.Type.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>add (object)](#apidoc.element.protobufjs.Type.prototype.add)
- description and source-code
```javascript
function add(object) {

    if (this.get(object.name))
        throw Error("duplicate name '" + object.name + "' in " + this);

    if (object instanceof Field && object.extend === undefined) {
        // NOTE: Extension fields aren't actual fields on the declaring type, but nested objects.
        // The root object takes care of adding distinct sister-fields to the respective extended
        // type instead.

        // avoids calling the getter if not absolutely necessary because it's called quite frequently
        if (this._fieldsById ? /* istanbul ignore next */ this._fieldsById[object.id] : this.fieldsById[object.id])
            throw Error("duplicate id " + object.id + " in " + this);
        if (this.isReservedId(object.id))
            throw Error("id " + object.id + " is reserved in " + this);
        if (this.isReservedName(object.name))
            throw Error("name '" + object.name + "' is reserved in " + this);

        if (object.parent)
            object.parent.remove(object);
        this.fields[object.name] = object;
        object.message = this;
        object.onAdd(this);
        return clearCache(this);
    }
    if (object instanceof OneOf) {
        if (!this.oneofs)
            this.oneofs = {};
        this.oneofs[object.name] = object;
        object.onAdd(this);
        return clearCache(this);
    }
    return Namespace.prototype.add.call(this, object);
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>constructor (name, options)](#apidoc.element.protobufjs.Type.prototype.constructor)
- description and source-code
```javascript
function Type(name, options) {
    Namespace.call(this, name, options);

    /**
     * Message fields.
     * @type {Object.<string,Field>}
     */
    this.fields = {};  // toJSON, marker

    /**
     * Oneofs declared within this namespace, if any.
     * @type {Object.<string,OneOf>}
     */
    this.oneofs = undefined; // toJSON

    /**
     * Extension ranges, if any.
     * @type {number[][]}
     */
    this.extensions = undefined; // toJSON

    /**
     * Reserved ranges, if any.
     * @type {Array.<number[]|string>}
     */
    this.reserved = undefined; // toJSON

    /*?
     * Whether this type is a legacy group.
     * @type {boolean|undefined}
     */
    this.group = undefined; // toJSON

    /**
     * Cached fields by id.
     * @type {?Object.<number,Field>}
     * @private
     */
    this._fieldsById = null;

    /**
     * Cached fields as an array.
     * @type {?Field[]}
     * @private
     */
    this._fieldsArray = null;

    /**
     * Cached oneofs as an array.
     * @type {?OneOf[]}
     * @private
     */
    this._oneofsArray = null;

    /**
     * Cached constructor.
     * @type {*}
     * @private
     */
    this._ctor = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.create"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>create (properties)](#apidoc.element.protobufjs.Type.prototype.create)
- description and source-code
```javascript
function create(properties) {
    return new this.ctor(properties);
}
```
- example usage
```shell
...
* **Message.decodeDelimited**(reader: 'Reader|Uint8Array'): 'Message'<br />
works like 'Message.decode' but additionally reads the length of the message prepended as a varint.

* **Message.create**(properties: 'Object'): 'Message'<br />
quickly creates a new runtime message from known to be valid properties without any conversion being performed. Where applicable
, it is recommended to prefer 'Message.create' over 'Message.fromObject'.

'''js
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.decode"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>decode (reader, length)](#apidoc.element.protobufjs.Type.prototype.decode)
- description and source-code
```javascript
function decode_setup(reader, length) {
    return this.setup().decode(reader, length); // overrides this method
}
```
- example usage
```shell
...
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.

'''js
try {
  var decodedMessage = AwesomeMessage.decode(buffer);
} catch (e) {
    if (e instanceof protobuf.util.ProtocolError) {
      // e.instance holds the so far decoded message with missing required fields
    } else {
      // wire format is invalid
    }
}
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.decodeDelimited"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>decodeDelimited (reader)](#apidoc.element.protobufjs.Type.prototype.decodeDelimited)
- description and source-code
```javascript
function decodeDelimited(reader) {
    if (!(reader instanceof Reader))
        reader = Reader.create(reader);
    return this.decode(reader, reader.uint32());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.encode"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>encode (message, writer)](#apidoc.element.protobufjs.Type.prototype.encode)
- description and source-code
```javascript
function encode_setup(message, writer) {
    return this.setup().encode(message, writer); // overrides this method
}
```
- example usage
```shell
...
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.

'''js
var buffer = AwesomeMessage.encode(message).finish();
'''

* **Message.encodeDelimited**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.encodeDelimited"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>encodeDelimited (message, writer)](#apidoc.element.protobufjs.Type.prototype.encodeDelimited)
- description and source-code
```javascript
function encodeDelimited(message, writer) {
    return this.encode(message, writer && writer.len ? writer.fork() : writer).ldelim();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.from"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>from (object)](#apidoc.element.protobufjs.Type.prototype.from)
- description and source-code
```javascript
function fromObject(object) {
    return this.setup().fromObject(object);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.fromObject"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>fromObject (object)](#apidoc.element.protobufjs.Type.prototype.fromObject)
- description and source-code
```javascript
function fromObject(object) {
    return this.setup().fromObject(object);
}
```
- example usage
```shell
...
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.get"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>get (name)](#apidoc.element.protobufjs.Type.prototype.get)
- description and source-code
```javascript
function get(name) {
    return this.fields[name]
        || this.oneofs && this.oneofs[name]
        || this.nested && this.nested[name]
        || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.isReservedId"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>isReservedId (id)](#apidoc.element.protobufjs.Type.prototype.isReservedId)
- description and source-code
```javascript
function isReservedId(id) {
    if (this.reserved)
        for (var i = 0; i < this.reserved.length; ++i)
            if (typeof this.reserved[i] !== "string" && this.reserved[i][0] <= id && this.reserved[i][1] >= id)
                return true;
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.isReservedName"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>isReservedName (name)](#apidoc.element.protobufjs.Type.prototype.isReservedName)
- description and source-code
```javascript
function isReservedName(name) {
    if (this.reserved)
        for (var i = 0; i < this.reserved.length; ++i)
            if (this.reserved[i] === name)
                return true;
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.remove"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>remove (object)](#apidoc.element.protobufjs.Type.prototype.remove)
- description and source-code
```javascript
function remove(object) {
    if (object instanceof Field && object.extend === undefined) {
        // See Type#add for the reason why extension fields are excluded here.

        /* istanbul ignore if */
        if (!this.fields || this.fields[object.name] !== object)
            throw Error(object + " is not a member of " + this);

        delete this.fields[object.name];
        object.parent = null;
        object.onRemove(this);
        return clearCache(this);
    }
    if (object instanceof OneOf) {

        /* istanbul ignore if */
        if (!this.oneofs || this.oneofs[object.name] !== object)
            throw Error(object + " is not a member of " + this);

        delete this.oneofs[object.name];
        object.parent = null;
        object.onRemove(this);
        return clearCache(this);
    }
    return Namespace.prototype.remove.call(this, object);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.resolveAll"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>resolveAll ()](#apidoc.element.protobufjs.Type.prototype.resolveAll)
- description and source-code
```javascript
function resolveAll() {
    var fields = this.fieldsArray, i = 0;
    while (i < fields.length)
        fields[i++].resolve();
    var oneofs = this.oneofsArray; i = 0;
    while (i < oneofs.length)
        oneofs[i++].resolve();
    return Namespace.prototype.resolve.call(this);
}
```
- example usage
```shell
...
if (process.argv[2] === "fromjson") {
json = require("../tests/data/test.json");
if (process.argv.indexOf("--resolve") < 0)
    for (var k = 0; k < 10000; ++k)
        protobuf.Root.fromJSON(json);
else
    for (var l = 0; l < 10000; ++l)
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.setup"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>setup ()](#apidoc.element.protobufjs.Type.prototype.setup)
- description and source-code
```javascript
function setup() {
    // Sets up everything at once so that the prototype chain does not have to be re-evaluated
    // multiple times (V8, soft-deopt prototype-check).
    var fullName = this.fullName,
        types    = [];
    for (var i = 0; i < /* initializes */ this.fieldsArray.length; ++i)
        types.push(this._fieldsArray[i].resolve().resolvedType);
    this.encode = encoder(this).eof(fullName + "$encode", {
        Writer : Writer,
        types  : types,
        util   : util
    });
    this.decode = decoder(this).eof(fullName + "$decode", {
        Reader : Reader,
        types  : types,
        util   : util
    });
    this.verify = verifier(this).eof(fullName + "$verify", {
        types : types,
        util  : util
    });
    this.fromObject = this.from = converter.fromObject(this).eof(fullName + "$fromObject", {
        types : types,
        util  : util
    });
    this.toObject = converter.toObject(this).eof(fullName + "$toObject", {
        types : types,
        util  : util
    });
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>toJSON ()](#apidoc.element.protobufjs.Type.prototype.toJSON)
- description and source-code
```javascript
function toJSON() {
    var inherited = Namespace.prototype.toJSON.call(this);
    return {
        options    : inherited && inherited.options || undefined,
        oneofs     : Namespace.arrayToJSON(this.oneofsArray),
        fields     : Namespace.arrayToJSON(this.fieldsArray.filter(function(obj) { return !obj.declaringField; })) || {},
        extensions : this.extensions && this.extensions.length ? this.extensions : undefined,
        reserved   : this.reserved && this.reserved.length ? this.reserved : undefined,
        group      : this.group || undefined,
        nested     : inherited && inherited.nested || undefined
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Type.prototype.toObject"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>toObject (message, options)](#apidoc.element.protobufjs.Type.prototype.toObject)
- description and source-code
```javascript
function toObject(message, options) {
    return this.setup().toObject(message, options);
}
```
- example usage
```shell
...
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
var object = AwesomeMessage.toObject(message, {
  enums: String,  // enums as string names
  longs: String,  // longs as strings (requires long.js)
  bytes: String,  // bytes as base64 encoded strings
  defaults: true, // includes default values
  arrays: true,   // populates empty arrays (repeated fields) even if defaults=false
  objects: true,  // populates empty objects (map fields) even if defaults=false
  oneofs: true    // includes virtual oneof fields set to the present field's name
...
```

#### <a name="apidoc.element.protobufjs.Type.prototype.verify"></a>[function <span class="apidocSignatureSpan">protobufjs.Type.prototype.</span>verify (message)](#apidoc.element.protobufjs.Type.prototype.verify)
- description and source-code
```javascript
function verify_setup(message) {
    return this.setup().verify(message); // overrides this method
}
```
- example usage
```shell
...
Note that **Message** below refers to any message type. See the next section for the definition of a [valid message](#valid-message
).

* **Message.verify**(message: 'Object'): 'null|string'<br />
explicitly performs verification prior to encoding a plain object. Instead of throwing, it returns the error message as a string
, if any.

'''js
var payload = "invalid (not an object)";
var err = AwesomeMessage.verify(payload);
if (err)
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.
...
```



# <a name="apidoc.module.protobufjs.Writer"></a>[module protobufjs.Writer](#apidoc.module.protobufjs.Writer)

#### <a name="apidoc.element.protobufjs.Writer.Writer"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>Writer ()](#apidoc.element.protobufjs.Writer.Writer)
- description and source-code
```javascript
function Writer() {

    /**
     * Current length.
     * @type {number}
     */
    this.len = 0;

    /**
     * Operations head.
     * @type {Object}
     */
    this.head = new Op(noop, 0, 0);

    /**
     * Operations tail
     * @type {Object}
     */
    this.tail = this.head;

    /**
     * Linked forked states.
     * @type {?Object}
     */
    this.states = null;

    // When a value is written, the writer calculates its byte length and puts it into a linked
    // list of operations to perform when finish() is called. This both allows us to allocate
    // buffers of the exact required size and reduces the amount of work we have to do compared
    // to first calculating over objects and then encoding over objects. In our case, the encoding
    // part is just a linked list walk calling operations with already prepared values.
}
```
- example usage
```shell
...
}

if (process.argv.length > 3 && /^\d+$/.test(process.argv[3]))
count = parseInt(process.argv[3], 10);
process.stdout.write(" x " + count + "\n");

function setupBrowser() {
protobuf.Writer.create = function create_browser() { return new protobuf.Writer(); };
protobuf.Reader.create = function create_browser(buf) { return new protobuf.Reader(buf); };
}

switch (process.argv[2]) {
case "encode-browser":
    setupBrowser();
    // eslint-disable-line no-fallthrough
...
```

#### <a name="apidoc.element.protobufjs.Writer._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.</span>_configure (BufferWriter_)](#apidoc.element.protobufjs.Writer._configure)
- description and source-code
```javascript
_configure = function (BufferWriter_) {
    BufferWriter = BufferWriter_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.alloc"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.</span>alloc (size)](#apidoc.element.protobufjs.Writer.alloc)
- description and source-code
```javascript
function pool_alloc(size) {
    if (size < 1 || size > MAX)
        return alloc(size);
    if (offset + size > SIZE) {
        slab = alloc(SIZE);
        offset = 0;
    }
    var buf = slice.call(slab, offset, offset += size);
    if (offset & 7) // align to 32 bit
        offset = (offset | 7) + 1;
    return buf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.create"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.</span>create ()](#apidoc.element.protobufjs.Writer.create)
- description and source-code
```javascript
function create_buffer_setup() {
    return (Writer.create = function create_buffer() {
        return new BufferWriter();
    })();
}
```
- example usage
```shell
...
* **Message.decodeDelimited**(reader: 'Reader|Uint8Array'): 'Message'<br />
works like 'Message.decode' but additionally reads the length of the message prepended as a varint.

* **Message.create**(properties: 'Object'): 'Message'<br />
quickly creates a new runtime message from known to be valid properties without any conversion being performed. Where applicable
, it is recommended to prefer 'Message.create' over 'Message.fromObject'.

'''js
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
...
```



# <a name="apidoc.module.protobufjs.Writer.prototype"></a>[module protobufjs.Writer.prototype](#apidoc.module.protobufjs.Writer.prototype)

#### <a name="apidoc.element.protobufjs.Writer.prototype.bool"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>bool (value)](#apidoc.element.protobufjs.Writer.prototype.bool)
- description and source-code
```javascript
function write_bool(value) {
    return this.push(writeByte, 1, value ? 1 : 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.bytes"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>bytes (value)](#apidoc.element.protobufjs.Writer.prototype.bytes)
- description and source-code
```javascript
function write_bytes(value) {
    var len = value.length >>> 0;
    if (!len)
        return this.push(writeByte, 1, 0);
    if (util.isString(value)) {
        var buf = Writer.alloc(len = base64.length(value));
        base64.decode(value, buf, 0);
        value = buf;
    }
    return this.uint32(len).push(writeBytes, len, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.double"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>double (value)](#apidoc.element.protobufjs.Writer.prototype.double)
- description and source-code
```javascript
function write_double(value) {
    return this.push(util.float.writeDoubleLE, 8, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.finish"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>finish ()](#apidoc.element.protobufjs.Writer.prototype.finish)
- description and source-code
```javascript
function finish() {
    var head = this.head.next, // skip noop
        buf  = this.constructor.alloc(this.len),
        pos  = 0;
    while (head) {
        head.fn(head.val, buf, pos);
        pos += head.len;
        head = head.next;
    }
    // this.head = this.tail = null;
    return buf;
}
```
- example usage
```shell
...
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.

'''js
var buffer = AwesomeMessage.encode(message).finish();
'''

* **Message.encodeDelimited**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.
...
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.fixed32"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fixed32 (value)](#apidoc.element.protobufjs.Writer.prototype.fixed32)
- description and source-code
```javascript
function write_fixed32(value) {
    return this.push(writeFixed32, 4, value >>> 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.fixed64"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fixed64 (value)](#apidoc.element.protobufjs.Writer.prototype.fixed64)
- description and source-code
```javascript
function write_fixed64(value) {
    var bits = LongBits.from(value);
    return this.push(writeFixed32, 4, bits.lo).push(writeFixed32, 4, bits.hi);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.float"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>float (value)](#apidoc.element.protobufjs.Writer.prototype.float)
- description and source-code
```javascript
function write_float(value) {
    return this.push(util.float.writeFloatLE, 4, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.fork"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>fork ()](#apidoc.element.protobufjs.Writer.prototype.fork)
- description and source-code
```javascript
function fork() {
    this.states = new State(this);
    this.head = this.tail = new Op(noop, 0, 0);
    this.len = 0;
    return this;
}
```
- example usage
```shell
...
* @param {string} ref Variable reference
* @returns {Codegen} Codegen instance
* @ignore
*/
function genTypePartial(gen, field, fieldIndex, ref) {
   return field.resolvedType.group
       ? gen("types[%d].encode(%s,w.uint32(%d)).uint32(%d)", fieldIndex, ref, (field.id << 3 | 3) >>> 0, (field.id << 3 | 4) >>>
0)
       : gen("types[%d].encode(%s,w.uint32(%d).fork()).ldelim()", fieldIndex, ref, (field.id << 3 | 2) >>> 0);
}

/**
* Generates an encoder specific to the specified message type.
* @param {Type} mtype Message type
* @returns {Codegen} Codegen instance
*/
...
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.int32"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>int32 (value)](#apidoc.element.protobufjs.Writer.prototype.int32)
- description and source-code
```javascript
function write_int32(value) {
    return value < 0
        ? this.push(writeVarint64, 10, LongBits.fromNumber(value)) // 10 bytes per spec
        : this.uint32(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.int64"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>int64 (value)](#apidoc.element.protobufjs.Writer.prototype.int64)
- description and source-code
```javascript
function write_uint64(value) {
    var bits = LongBits.from(value);
    return this.push(writeVarint64, bits.length(), bits);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.ldelim"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>ldelim ()](#apidoc.element.protobufjs.Writer.prototype.ldelim)
- description and source-code
```javascript
function ldelim() {
    var head = this.head,
        tail = this.tail,
        len  = this.len;
    this.reset().uint32(len);
    if (len) {
        this.tail.next = head.next; // skip noop
        this.tail = tail;
        this.len += len;
    }
    return this;
}
```
- example usage
```shell
...
* @param {string} ref Variable reference
* @returns {Codegen} Codegen instance
* @ignore
*/
function genTypePartial(gen, field, fieldIndex, ref) {
   return field.resolvedType.group
       ? gen("types[%d].encode(%s,w.uint32(%d)).uint32(%d)", fieldIndex, ref, (field.id << 3 | 3) >>> 0, (field.id << 3 | 4) >>>
0)
       : gen("types[%d].encode(%s,w.uint32(%d).fork()).ldelim()", fieldIndex, ref, (field.id << 3 | 2) >>> 0);
}

/**
* Generates an encoder specific to the specified message type.
* @param {Type} mtype Message type
* @returns {Codegen} Codegen instance
*/
...
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.push"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>push (fn, len, val)](#apidoc.element.protobufjs.Writer.prototype.push)
- description and source-code
```javascript
function push(fn, len, val) {
    this.tail = this.tail.next = new Op(fn, len, val);
    this.len += len;
    return this;
}
```
- example usage
```shell
...
// https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object/keys
if (!Object.keys) {
  Object.keys = function (o) {
    if (o !== Object(o)) { throw TypeError('Object.keys called on non-object'); }
    var ret = [], p;
    for (p in o) {
      if (Object.prototype.hasOwnProperty.call(o, p)) {
        ret.push(p);
      }
    }
    return ret;
  };
}

// ES5 15.4.3.2 Array.isArray ( arg )
...
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.reset"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>reset ()](#apidoc.element.protobufjs.Writer.prototype.reset)
- description and source-code
```javascript
function reset() {
    if (this.states) {
        this.head   = this.states.head;
        this.tail   = this.states.tail;
        this.len    = this.states.len;
        this.states = this.states.next;
    } else {
        this.head = this.tail = new Op(noop, 0, 0);
        this.len  = 0;
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.sfixed32"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sfixed32 (value)](#apidoc.element.protobufjs.Writer.prototype.sfixed32)
- description and source-code
```javascript
function write_fixed32(value) {
    return this.push(writeFixed32, 4, value >>> 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.sfixed64"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sfixed64 (value)](#apidoc.element.protobufjs.Writer.prototype.sfixed64)
- description and source-code
```javascript
function write_fixed64(value) {
    var bits = LongBits.from(value);
    return this.push(writeFixed32, 4, bits.lo).push(writeFixed32, 4, bits.hi);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.sint32"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sint32 (value)](#apidoc.element.protobufjs.Writer.prototype.sint32)
- description and source-code
```javascript
function write_sint32(value) {
    return this.uint32((value << 1 ^ value >> 31) >>> 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.sint64"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>sint64 (value)](#apidoc.element.protobufjs.Writer.prototype.sint64)
- description and source-code
```javascript
function write_sint64(value) {
    var bits = LongBits.from(value).zzEncode();
    return this.push(writeVarint64, bits.length(), bits);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.string"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>string (value)](#apidoc.element.protobufjs.Writer.prototype.string)
- description and source-code
```javascript
function write_string(value) {
    var len = utf8.length(value);
    return len
        ? this.uint32(len).push(utf8.write, len, value)
        : this.push(writeByte, 1, 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.uint32"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>uint32 (value)](#apidoc.element.protobufjs.Writer.prototype.uint32)
- description and source-code
```javascript
function write_uint32(value) {
    // here, the call to this.push has been inlined and a varint specific Op subclass is used.
    // uint32 is by far the most frequently used operation and benefits significantly from this.
    this.len += (this.tail = this.tail.next = new VarintOp(
        (value = value >>> 0)
                < 128       ? 1
        : value < 16384     ? 2
        : value < 2097152   ? 3
        : value < 268435456 ? 4
        :                     5,
    value)).len;
    return this;
}
```
- example usage
```shell
...
function decoder(mtype) {
/* eslint-disable no-unexpected-multiline */
var gen = util.codegen("r", "l")
("if(!(r instanceof Reader))")
    ("r=Reader.create(r)")
("var c=l===undefined?r.len:r.pos+l,m=new this.ctor" + (mtype.fieldsArray.filter(function(field) { return field.map; }).length ? ",
k" : ""))
("while(r.pos<c){")
    ("var t=r.uint32()");
if (mtype.group) gen
    ("if((t&7)===4)")
        ("break");
gen
    ("switch(t>>>3){");

var i = 0;
...
```

#### <a name="apidoc.element.protobufjs.Writer.prototype.uint64"></a>[function <span class="apidocSignatureSpan">protobufjs.Writer.prototype.</span>uint64 (value)](#apidoc.element.protobufjs.Writer.prototype.uint64)
- description and source-code
```javascript
function write_uint64(value) {
    var bits = LongBits.from(value);
    return this.push(writeVarint64, bits.length(), bits);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.converter"></a>[module protobufjs.converter](#apidoc.module.protobufjs.converter)

#### <a name="apidoc.element.protobufjs.converter.fromObject"></a>[function <span class="apidocSignatureSpan">protobufjs.converter.</span>fromObject (mtype)](#apidoc.element.protobufjs.converter.fromObject)
- description and source-code
```javascript
function fromObject(mtype) {
    /* eslint-disable no-unexpected-multiline, block-scoped-var, no-redeclare */
    var fields = mtype.fieldsArray;
    var gen = util.codegen("d")
    ("if(d instanceof this.ctor)")
        ("return d");
    if (!fields.length) return gen
    ("return new this.ctor");
    gen
    ("var m=new this.ctor");
    for (var i = 0; i < fields.length; ++i) {
        var field  = fields[i].resolve(),
            prop   = util.safeProp(field.name);

        // Map fields
        if (field.map) { gen
    ("if(d%s){", prop)
        ("if(typeof d%s!==\"object\")", prop)
            ("throw TypeError(%j)", field.fullName + ": object expected")
        ("m%s={}", prop)
        ("for(var ks=Object.keys(d%s),i=0;i<ks.length;++i){", prop);
            genValuePartial_fromObject(gen, field, /* not sorted */ i, prop + "[ks[i]]")
        ("}")
    ("}");

        // Repeated fields
        } else if (field.repeated) { gen
    ("if(d%s){", prop)
        ("if(!Array.isArray(d%s))", prop)
            ("throw TypeError(%j)", field.fullName + ": array expected")
        ("m%s=[]", prop)
        ("for(var i=0;i<d%s.length;++i){", prop);
            genValuePartial_fromObject(gen, field, /* not sorted */ i, prop + "[i]")
        ("}")
    ("}");

        // Non-repeated fields
        } else {
            if (!(field.resolvedType instanceof Enum)) gen // no need to test for null/undefined if an enum (uses switch)
    ("if(d%s!=null){", prop); // !== undefined && !== null
        genValuePartial_fromObject(gen, field, /* not sorted */ i, prop);
            if (!(field.resolvedType instanceof Enum)) gen
    ("}");
        }
    } return gen
    ("return m");
    /* eslint-enable no-unexpected-multiline, block-scoped-var, no-redeclare */
}
```
- example usage
```shell
...
var message = AwesomeMessage.create({ awesomeField: "AwesomeString" });
'''

* **Message.fromObject**(object: 'Object'): 'Message'<br />
converts any plain object to a runtime message. Tries to convert whatever is specified (use 'Message.verify' before if necessary
).

'''js
var message = AwesomeMessage.fromObject({ awesomeField: 42 });
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
...
```

#### <a name="apidoc.element.protobufjs.converter.toObject"></a>[function <span class="apidocSignatureSpan">protobufjs.converter.</span>toObject (mtype)](#apidoc.element.protobufjs.converter.toObject)
- description and source-code
```javascript
function toObject(mtype) {
    /* eslint-disable no-unexpected-multiline, block-scoped-var, no-redeclare */
    var fields = mtype.fieldsArray.slice().sort(util.compareFieldsById);
    if (!fields.length)
        return util.codegen()("return {}");
    var gen = util.codegen("m", "o")
    ("if(!o)")
        ("o={}")
    ("var d={}");

    var repeatedFields = [],
        mapFields = [],
        normalFields = [],
        i = 0;
    for (; i < fields.length; ++i)
        if (!fields[i].partOf)
            ( fields[i].resolve().repeated ? repeatedFields
            : fields[i].map ? mapFields
            : normalFields).push(fields[i]);

    if (repeatedFields.length) { gen
    ("if(o.arrays||o.defaults){");
        for (i = 0; i < repeatedFields.length; ++i) gen
        ("d%s=[]", util.safeProp(repeatedFields[i].name));
        gen
    ("}");
    }

    if (mapFields.length) { gen
    ("if(o.objects||o.defaults){");
        for (i = 0; i < mapFields.length; ++i) gen
        ("d%s={}", util.safeProp(mapFields[i].name));
        gen
    ("}");
    }

    if (normalFields.length) { gen
    ("if(o.defaults){");
        for (i = 0; i < normalFields.length; ++i) {
            var field = normalFields[i],
                prop  = util.safeProp(field.name);
            if (field.resolvedType instanceof Enum) gen
        ("d%s=o.enums===String?%j:%j", prop, field.resolvedType.valuesById[field.typeDefault], field.typeDefault);
            else if (field.long) gen
        ("if(util.Long){")
            ("var n=new util.Long(%d,%d,%j)", field.typeDefault.low, field.typeDefault.high, field.typeDefault.unsigned)
            ("d%s=o.longs===String?n.toString():o.longs===Number?n.toNumber():n", prop)
        ("}else")
            ("d%s=o.longs===String?%j:%d", prop, field.typeDefault.toString(), field.typeDefault.toNumber());
            else if (field.bytes) gen
        ("d%s=o.bytes===String?%j:%s", prop, String.fromCharCode.apply(String, field.typeDefault), "[" + Array.prototype.slice.call
(field.typeDefault).join(",") + "]");
            else gen
        ("d%s=%j", prop, field.typeDefault); // also messages (=null)
        } gen
    ("}");
    }
    var hasKs2 = false;
    for (i = 0; i < fields.length; ++i) {
        var field = fields[i],
            index = mtype._fieldsArray.indexOf(field),
            prop  = util.safeProp(field.name);
        if (field.map) {
            if (!hasKs2) { hasKs2 = true; gen
    ("var ks2");
            } gen
    ("if(m%s&&(ks2=Object.keys(m%s)).length){", prop, prop)
        ("d%s={}", prop)
        ("for(var j=0;j<ks2.length;++j){");
            genValuePartial_toObject(gen, field, /* sorted */ index, prop + "[ks2[j]]")
        ("}");
        } else if (field.repeated) { gen
    ("if(m%s&&m%s.length){", prop, prop)
        ("d%s=[]", prop)
        ("for(var j=0;j<m%s.length;++j){", prop);
            genValuePartial_toObject(gen, field, /* sorted */ index, prop + "[j]")
        ("}");
        } else { gen
    ("if(m%s!=null&&m.hasOwnProperty(%j)){", prop, field.name); // !== undefined && !== null
        genValuePartial_toObject(gen, field, /* sorted */ index, prop);
        if (field.partOf) gen
        ("if(o.oneofs)")
            ("d%s=%j", util.safeProp(field.partOf.name), field.name);
        }
        gen
    ("}");
    }
    return gen
    ("return d");
    /* eslint-enable no-unexpected-multiline, block-scoped-var, no-redeclare */
}
```
- example usage
```shell
...
// converts awesomeField to a string
'''

* **Message.toObject**(message: 'Message' [, options: 'ConversionOptions']): 'Object'<br />
converts a runtime message to a plain object.

'''js
var object = AwesomeMessage.toObject(message, {
  enums: String,  // enums as string names
  longs: String,  // longs as strings (requires long.js)
  bytes: String,  // bytes as base64 encoded strings
  defaults: true, // includes default values
  arrays: true,   // populates empty arrays (repeated fields) even if defaults=false
  objects: true,  // populates empty objects (map fields) even if defaults=false
  oneofs: true    // includes virtual oneof fields set to the present field's name
...
```



# <a name="apidoc.module.protobufjs.debug"></a>[module protobufjs.debug](#apidoc.module.protobufjs.debug)

#### <a name="apidoc.element.protobufjs.debug.disable"></a>[function <span class="apidocSignatureSpan">protobufjs.debug.</span>disable ()](#apidoc.element.protobufjs.debug.disable)
- description and source-code
```javascript
function disable() {
    protobuf.util.codegen = codegen;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.debug.enable"></a>[function <span class="apidocSignatureSpan">protobufjs.debug.</span>enable ()](#apidoc.element.protobufjs.debug.enable)
- description and source-code
```javascript
function enable() {
    protobuf.util.codegen = codegen_debug;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.debug.unusedTypes"></a>[function <span class="apidocSignatureSpan">protobufjs.debug.</span>unusedTypes (ns)](#apidoc.element.protobufjs.debug.unusedTypes)
- description and source-code
```javascript
function unusedTypes(ns) {

    /* istanbul ignore if */
    if (!(ns instanceof protobuf.Namespace))
        throw TypeError("ns must be a Namespace");

    /* istanbul ignore if */
    if (!ns.nested)
        return [];

    var unused = [];
    for (var names = Object.keys(ns.nested), i = 0; i < names.length; ++i) {
        var nested = ns.nested[names[i]];
        if (nested instanceof protobuf.Type) {
            var calls = (nested.encode.calls|0)
                      + (nested.decode.calls|0)
                      + (nested.verify.calls|0)
                      + (nested.toObject.calls|0)
                      + (nested.fromObject.calls|0);
            if (!calls)
                unused.push(nested);
        } else if (nested instanceof protobuf.Namespace)
            Array.prototype.push.apply(unused, unusedTypes(nested));
    }
    return unused;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.rpc"></a>[module protobufjs.rpc](#apidoc.module.protobufjs.rpc)

#### <a name="apidoc.element.protobufjs.rpc.Service"></a>[function <span class="apidocSignatureSpan">protobufjs.rpc.</span>Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service)
- description and source-code
```javascript
function Service(rpcImpl, requestDelimited, responseDelimited) {

    if (typeof rpcImpl !== "function")
        throw TypeError("rpcImpl must be a function");

    util.EventEmitter.call(this);

    /**
     * RPC implementation. Becomes 'null' once the service is ended.
     * @type {?RPCImpl}
     */
    this.rpcImpl = rpcImpl;

    /**
     * Whether requests are length-delimited.
     * @type {boolean}
     */
    this.requestDelimited = Boolean(requestDelimited);

    /**
     * Whether responses are length-delimited.
     * @type {boolean}
     */
    this.responseDelimited = Boolean(responseDelimited);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.rpc.Service"></a>[module protobufjs.rpc.Service](#apidoc.module.protobufjs.rpc.Service)

#### <a name="apidoc.element.protobufjs.rpc.Service.Service"></a>[function <span class="apidocSignatureSpan">protobufjs.rpc.</span>Service (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service.Service)
- description and source-code
```javascript
function Service(rpcImpl, requestDelimited, responseDelimited) {

    if (typeof rpcImpl !== "function")
        throw TypeError("rpcImpl must be a function");

    util.EventEmitter.call(this);

    /**
     * RPC implementation. Becomes 'null' once the service is ended.
     * @type {?RPCImpl}
     */
    this.rpcImpl = rpcImpl;

    /**
     * Whether requests are length-delimited.
     * @type {boolean}
     */
    this.requestDelimited = Boolean(requestDelimited);

    /**
     * Whether responses are length-delimited.
     * @type {boolean}
     */
    this.responseDelimited = Boolean(responseDelimited);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.rpc.Service.prototype"></a>[module protobufjs.rpc.Service.prototype](#apidoc.module.protobufjs.rpc.Service.prototype)

#### <a name="apidoc.element.protobufjs.rpc.Service.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>constructor (rpcImpl, requestDelimited, responseDelimited)](#apidoc.element.protobufjs.rpc.Service.prototype.constructor)
- description and source-code
```javascript
function Service(rpcImpl, requestDelimited, responseDelimited) {

    if (typeof rpcImpl !== "function")
        throw TypeError("rpcImpl must be a function");

    util.EventEmitter.call(this);

    /**
     * RPC implementation. Becomes 'null' once the service is ended.
     * @type {?RPCImpl}
     */
    this.rpcImpl = rpcImpl;

    /**
     * Whether requests are length-delimited.
     * @type {boolean}
     */
    this.requestDelimited = Boolean(requestDelimited);

    /**
     * Whether responses are length-delimited.
     * @type {boolean}
     */
    this.responseDelimited = Boolean(responseDelimited);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.rpc.Service.prototype.end"></a>[function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>end (endedByRPC)](#apidoc.element.protobufjs.rpc.Service.prototype.end)
- description and source-code
```javascript
function end(endedByRPC) {
    if (this.rpcImpl) {
        if (!endedByRPC) // signal end to rpcImpl
            this.rpcImpl(null, null, null);
        this.rpcImpl = null;
        this.emit("end").off();
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.rpc.Service.prototype.rpcCall"></a>[function <span class="apidocSignatureSpan">protobufjs.rpc.Service.prototype.</span>rpcCall (method, requestCtor, responseCtor, request, callback)](#apidoc.element.protobufjs.rpc.Service.prototype.rpcCall)
- description and source-code
```javascript
function rpcCall(method, requestCtor, responseCtor, request, callback) {

    if (!request)
        throw TypeError("request must be specified");

    var self = this;
    if (!callback)
        return util.asPromise(rpcCall, self, method, requestCtor, responseCtor, request);

    if (!self.rpcImpl) {
        setTimeout(function() { callback(Error("already ended")); }, 0);
        return undefined;
    }

    try {
        return self.rpcImpl(
            method,
            requestCtor[self.requestDelimited ? "encodeDelimited" : "encode"](request).finish(),
            function rpcCallback(err, response) {

                if (err) {
                    self.emit("error", err, method);
                    return callback(err);
                }

                if (response === null) {
                    self.end(/* endedByRPC */ true);
                    return undefined;
                }

                if (!(response instanceof responseCtor)) {
                    try {
                        response = responseCtor[self.responseDelimited ? "decodeDelimited" : "decode"](response);
                    } catch (err) {
                        self.emit("error", err, method);
                        return callback(err);
                    }
                }

                self.emit("data", response, method);
                return callback(null, response);
            }
        );
    } catch (err) {
        self.emit("error", err, method);
        setTimeout(function() { callback(err); }, 0);
        return undefined;
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.tokenize"></a>[module protobufjs.tokenize](#apidoc.module.protobufjs.tokenize)

#### <a name="apidoc.element.protobufjs.tokenize.tokenize"></a>[function <span class="apidocSignatureSpan">protobufjs.</span>tokenize (source)](#apidoc.element.protobufjs.tokenize.tokenize)
- description and source-code
```javascript
function tokenize(source) {
    /* eslint-disable callback-return */
    source = source.toString();

    var offset = 0,
        length = source.length,
        line = 1,
        commentType = null,
        commentText = null,
        commentLine = 0;

    var stack = [];

    var stringDelim = null;

    /* istanbul ignore next */
    /**
     * Creates an error for illegal syntax.
     * @param {string} subject Subject
     * @returns {Error} Error created
     * @inner
     */
    function illegal(subject) {
        return Error("illegal " + subject + " (line " + line + ")");
    }

    /**
     * Reads a string till its end.
     * @returns {string} String read
     * @inner
     */
    function readString() {
        var re = stringDelim === "'" ? stringSingleRe : stringDoubleRe;
        re.lastIndex = offset - 1;
        var match = re.exec(source);
        if (!match)
            throw illegal("string");
        offset = re.lastIndex;
        push(stringDelim);
        stringDelim = null;
        return unescape(match[1]);
    }

    /**
     * Gets the character at 'pos' within the source.
     * @param {number} pos Position
     * @returns {string} Character
     * @inner
     */
    function charAt(pos) {
        return source.charAt(pos);
    }

    /**
     * Sets the current comment text.
     * @param {number} start Start offset
     * @param {number} end End offset
     * @returns {undefined}
     * @inner
     */
    function setComment(start, end) {
        commentType = source.charAt(start++);
        commentLine = line;
        var lines = source
            .substring(start, end)
            .split(setCommentSplitRe);
        for (var i = 0; i < lines.length; ++i)
            lines[i] = lines[i].replace(setCommentRe, "").trim();
        commentText = lines
            .join("\n")
            .trim();
    }

    /**
     * Obtains the next token.
     * @returns {?string} Next token or 'null' on eof
     * @inner
     */
    function next() {
        if (stack.length > 0)
            return stack.shift();
        if (stringDelim)
            return readString();
        var repeat,
            prev,
            curr,
            start,
            isComment;
        do {
            if (offset === length)
                return null;
            repeat = false;
            while (whitespaceRe.test(curr = charAt(offset))) {
                if (curr === "\n")
                    ++line;
                if (++offset === length)
                    return null;
            }
            if (charAt(offset) === "/") {
                if (++offset === length)
                    throw illegal("comment");
                if (charAt(offset) === "/") { // Line
                    isComment = charAt(start = offset + 1) === "/";
                    while (charAt(++offset) !== "\n")
                        if (offset === length)
                            return null;
                    ++offset;
                    if (isComment)
                        setComment(start, offset - 1);
                    ++line;
                    repeat = true;
                } else if ((curr = charAt(offset)) === "*") { /* Block */
                    isComment = charAt(start = offset + 1) === "*";
                    do {
                        if (curr === "\n")
                            ++line;
                        if (++offset === length)
                            throw illegal("comment");
                        prev = curr;
                        curr = charAt(offset);
                    } while (prev !== "*" || curr !== "/");
                    ++offset;
                    if (isComment)
                        setComment(start, offset - 2);
                    repeat = true;
                } else
                    return "/";
            }
        } while (repeat);

        // offset !== length if we got here

        var end = offset;
        delimRe.lastIndex = 0; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.tokenize.unescape"></a>[function <span class="apidocSignatureSpan">protobufjs.tokenize.</span>unescape (str)](#apidoc.element.protobufjs.tokenize.unescape)
- description and source-code
```javascript
function unescape(str) {
    return str.replace(unescapeRe, function($0, $1) {
        switch ($1) {
            case "\\":
            case "":
                return $1;
            default:
                return unescapeMap[$1] || "";
        }
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util"></a>[module protobufjs.util](#apidoc.module.protobufjs.util)

#### <a name="apidoc.element.protobufjs.util.Array"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>Array ()](#apidoc.element.protobufjs.util.Array)
- description and source-code
```javascript
function Uint8Array() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.EventEmitter"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {

    /**
     * Registered listeners.
     * @type {Object.<string,*>}
     * @private
     */
    this._listeners = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long)
- description and source-code
```javascript
function Long(low, high, unsigned) {

    /**
     * The low 32 bits as a signed value.
     * @type {number}
     */
    this.low = low | 0;

    /**
     * The high 32 bits as a signed value.
     * @type {number}
     */
    this.high = high | 0;

    /**
     * Whether unsigned or not.
     * @type {boolean}
     */
    this.unsigned = !!unsigned;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits)
- description and source-code
```javascript
function LongBits(lo, hi) {

    // note that the casts below are theoretically unnecessary as of today, but older statically
    // generated converter code might still call the ctor with signed 32bits. kept for compat.

    /**
     * Low bits.
     * @type {number}
     */
    this.lo = lo >>> 0;

    /**
     * High bits.
     * @type {number}
     */
    this.hi = hi >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.ProtocolError"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError)
- description and source-code
```javascript
function CustomError(message, properties) {

    if (!(this instanceof CustomError))
        return new CustomError(message, properties);

    // Error.call(this, message);
    // ^ just returns a new error instance because the ctor can be called as a function

    Object.defineProperty(this, "message", { get: function() { return message; } });

    /* istanbul ignore next */
    if (Error.captureStackTrace) // node
        Error.captureStackTrace(this, CustomError);
    else
        Object.defineProperty(this, "stack", { value: (new Error()).stack || "" });

    if (properties)
        merge(this, properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util._Buffer_allocUnsafe"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>_Buffer_allocUnsafe (size)](#apidoc.element.protobufjs.util._Buffer_allocUnsafe)
- description and source-code
```javascript
_Buffer_allocUnsafe = function (size) {
  assertSize(size);
  return allocate(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util._Buffer_from"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>_Buffer_from (value, encodingOrOffset, length)](#apidoc.element.protobufjs.util._Buffer_from)
- description and source-code
```javascript
_Buffer_from = function (value, encodingOrOffset, length) {
  if (typeof value === 'number')
    throw new TypeError('"value" argument must not be a number');

  if (isArrayBuffer(value) || isSharedArrayBuffer(value))
    return fromArrayBuffer(value, encodingOrOffset, length);

  if (typeof value === 'string')
    return fromString(value, encodingOrOffset);

  return fromObject(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util._configure"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>_configure ()](#apidoc.element.protobufjs.util._configure)
- description and source-code
```javascript
_configure = function () {
    var Buffer = util.Buffer;
    /* istanbul ignore if */
    if (!Buffer) {
        util._Buffer_from = util._Buffer_allocUnsafe = null;
        return;
    }
    // because node 4.x buffers are incompatible & immutable
    // see: https://github.com/dcodeIO/protobuf.js/pull/665
    util._Buffer_from = Buffer.from !== Uint8Array.from && Buffer.from ||
        /* istanbul ignore next */
        function Buffer_from(value, encoding) {
            return new Buffer(value, encoding);
        };
    util._Buffer_allocUnsafe = Buffer.allocUnsafe ||
        /* istanbul ignore next */
        function Buffer_allocUnsafe(size) {
            return new Buffer(size);
        };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.asPromise"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>asPromise (fn, ctx)](#apidoc.element.protobufjs.util.asPromise)
- description and source-code
```javascript
function asPromise(fn, ctx) {
    var params = [];
    for (var i = 2; i < arguments.length;)
        params.push(arguments[i++]);
    var pending = true;
    return new Promise(function asPromiseExecutor(resolve, reject) {
        params.push(function asPromiseCallback(err/*, varargs */) {
            if (pending) {
                pending = false;
                if (err)
                    reject(err);
                else {
                    var args = [];
                    for (var i = 1; i < arguments.length;)
                        args.push(arguments[i++]);
                    resolve.apply(null, args);
                }
            }
        });
        try {
            fn.apply(ctx || this, params); // eslint-disable-line no-invalid-this
        } catch (err) {
            if (pending) {
                pending = false;
                reject(err);
            }
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.codegen"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>codegen ()](#apidoc.element.protobufjs.util.codegen)
- description and source-code
```javascript
function codegen() {
    var params = [],
        src    = [],
        indent = 1,
        inCase = false;
    for (var i = 0; i < arguments.length;)
        params.push(arguments[i++]);

    /**
     * A codegen instance as returned by {@link codegen}, that also is a sprintf-like appender function.
     * @typedef Codegen
     * @type {function}
     * @param {string} format Format string
     * @param {...*} args Replacements
     * @returns {Codegen} Itself
     * @property {function(string=):string} str Stringifies the so far generated function source.
     * @property {function(string=, Object=):function} eof Ends generation and builds the function whilst applying a scope.
     */
    /**/
    function gen() {
        var args = [],
            i = 0;
        for (; i < arguments.length;)
            args.push(arguments[i++]);
        var line = sprintf.apply(null, args);
        var level = indent;
        if (src.length) {
            var prev = src[src.length - 1];

            // block open or one time branch
            if (blockOpenRe.test(prev))
                level = ++indent; // keep
            else if (branchRe.test(prev))
                ++level; // once

            // casing
            if (casingRe.test(prev) && !casingRe.test(line)) {
                level = ++indent;
                inCase = true;
            } else if (inCase && breakRe.test(prev)) {
                level = --indent;
                inCase = false;
            }

            // block close
            if (blockCloseRe.test(line))
                level = --indent;
        }
        for (i = 0; i < level; ++i)
            line = "\t" + line;
        src.push(line);
        return gen;
    }

    /**
     * Stringifies the so far generated function source.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @returns {string} Function source using tabs for indentation
     * @inner
     */
    function str(name) {
        return "function" + (name ? " " + name.replace(/[^\w_$]/g, "_") : "") + "(" + params.join(",") + ") {\n" + src.join("\n") + "\n}";
    }

    gen.str = str;

    /**
     * Ends generation and builds the function whilst applying a scope.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @param {Object.<string,*>} [scope] Function scope
     * @returns {function} The generated function, with scope applied if specified
     * @inner
     */
    function eof(name, scope) {
        if (typeof name === "object") {
            scope = name;
            name = undefined;
        }
        var source = gen.str(name);
        if (codegen.verbose)
            console.log("--- codegen ---\n" + source.replace(/^/mg, "> ").replace(/\t/g, "  ")); // eslint-disable-line no-console
        var keys = Object.keys(scope || (scope = {}));
        return Function.apply(null, keys.concat("return " + source)).apply(null, keys.map(function(key) { return scope[key]; })); //
eslint-disable-line no-new-func
        //     ^ Creates a wrapper function with the scoped variable names as its parameters,
        //       calls it with the respective scoped variable values ^
        //       and returns our brand-new properly scoped function.
        //
        // This works because "Invoking the Function constructor as a function (without using the
        // new operator) has the same effect as invoking it as a constructor."
        // https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Function
    }

    gen.eof = eof;

    return gen;
}
```
- example usage
```shell
...
/**
 * Generates a decoder specific to the specified message type.
 * @param {Type} mtype Message type
 * @returns {Codegen} Codegen instance
 */
function decoder(mtype) {
/* eslint-disable no-unexpected-multiline */
var gen = util.codegen("r", "l")
("if(!(r instanceof Reader))")
    ("r=Reader.create(r)")
("var c=l===undefined?r.len:r.pos+l,m=new this.ctor" + (mtype.fieldsArray.filter(function(field) { return field.map; }).length ? ",
k" : ""))
("while(r.pos<c){")
    ("var t=r.uint32()");
if (mtype.group) gen
    ("if((t&7)===4)")
...
```

#### <a name="apidoc.element.protobufjs.util.compareFieldsById"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>compareFieldsById (a, b)](#apidoc.element.protobufjs.util.compareFieldsById)
- description and source-code
```javascript
function compareFieldsById(a, b) {
    return a.id - b.id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.fetch"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch)
- description and source-code
```javascript
function fetch(filename, options, callback) {
    if (typeof options === "function") {
        callback = options;
        options = {};
    } else if (!options)
        options = {};

    if (!callback)
        return asPromise(fetch, this, filename, options); // eslint-disable-line no-invalid-this

    // if a node-like filesystem is present, try it first but fall back to XHR if nothing is found.
    if (!options.xhr && fs && fs.readFile)
        return fs.readFile(filename, function fetchReadFileCallback(err, contents) {
            return err && typeof XMLHttpRequest !== "undefined"
                ? fetch.xhr(filename, options, callback)
                : err
                ? callback(err)
                : callback(null, options.binary ? contents : contents.toString("utf8"));
        });

    // use the XHR version otherwise.
    return fetch.xhr(filename, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>float (exports)](#apidoc.element.protobufjs.util.float)
- description and source-code
```javascript
function factory(exports) {

    // float: typed array
    if (typeof Float32Array !== "undefined") (function() {

        var f32 = new Float32Array([ -0 ]),
            f8b = new Uint8Array(f32.buffer),
            le  = f8b[3] === 128;

        function writeFloat_f32_cpy(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
        }

        function writeFloat_f32_rev(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[3];
            buf[pos + 1] = f8b[2];
            buf[pos + 2] = f8b[1];
            buf[pos + 3] = f8b[0];
        }

        /* istanbul ignore next */
        exports.writeFloatLE = le ? writeFloat_f32_cpy : writeFloat_f32_rev;
        /* istanbul ignore next */
        exports.writeFloatBE = le ? writeFloat_f32_rev : writeFloat_f32_cpy;

        function readFloat_f32_cpy(buf, pos) {
            f8b[0] = buf[pos    ];
            f8b[1] = buf[pos + 1];
            f8b[2] = buf[pos + 2];
            f8b[3] = buf[pos + 3];
            return f32[0];
        }

        function readFloat_f32_rev(buf, pos) {
            f8b[3] = buf[pos    ];
            f8b[2] = buf[pos + 1];
            f8b[1] = buf[pos + 2];
            f8b[0] = buf[pos + 3];
            return f32[0];
        }

        /* istanbul ignore next */
        exports.readFloatLE = le ? readFloat_f32_cpy : readFloat_f32_rev;
        /* istanbul ignore next */
        exports.readFloatBE = le ? readFloat_f32_rev : readFloat_f32_cpy;

    // float: ieee754
    })(); else (function() {

        function writeFloat_ieee754(writeUint, val, buf, pos) {
            var sign = val < 0 ? 1 : 0;
            if (sign)
                val = -val;
            if (val === 0)
                writeUint(1 / val > 0 ? /* positive */ 0 : /* negative 0 */ 2147483648, buf, pos);
            else if (isNaN(val))
                writeUint(2143289344, buf, pos);
            else if (val > 3.4028234663852886e+38) // +-Infinity
                writeUint((sign << 31 | 2139095040) >>> 0, buf, pos);
            else if (val < 1.1754943508222875e-38) // denormal
                writeUint((sign << 31 | Math.round(val / 1.401298464324817e-45)) >>> 0, buf, pos);
            else {
                var exponent = Math.floor(Math.log(val) / Math.LN2),
                    mantissa = Math.round(val * Math.pow(2, -exponent) * 8388608) & 8388607;
                writeUint((sign << 31 | exponent + 127 << 23 | mantissa) >>> 0, buf, pos);
            }
        }

        exports.writeFloatLE = writeFloat_ieee754.bind(null, writeUintLE);
        exports.writeFloatBE = writeFloat_ieee754.bind(null, writeUintBE);

        function readFloat_ieee754(readUint, buf, pos) {
            var uint = readUint(buf, pos),
                sign = (uint >> 31) * 2 + 1,
                exponent = uint >>> 23 & 255,
                mantissa = uint & 8388607;
            return exponent === 255
                ? mantissa
                ? NaN
                : sign * Infinity
                : exponent === 0 // denormal
                ? sign * 1.401298464324817e-45 * mantissa
                : sign * Math.pow(2, exponent - 150) * (mantissa + 8388608);
        }

        exports.readFloatLE = readFloat_ieee754.bind(null, readUintLE);
        exports.readFloatBE = readFloat_ieee754.bind(null, readUintBE);

    })();

    // double: typed array
    if (typeof Float64Array !== "undefined") (function() {

        var f64 = new Float64Array([-0]),
            f8b = new Uint8Array(f64.buffer),
            le  = f8b[7] === 128;

        function writeDouble_f64_cpy(val, buf, pos) {
            f64[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
            buf[pos + 4] = f8b[4];
            buf[pos + 5] = f8b[5];
            buf[pos + 6] = f8b[6] ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.inquire"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>inquire (moduleName)](#apidoc.element.protobufjs.util.inquire)
- description and source-code
```javascript
function inquire(moduleName) {
    try {
        var mod = eval("quire".replace(/^/,"re"))(moduleName); // eslint-disable-line no-eval
        if (mod && (mod.length || Object.keys(mod).length))
            return mod;
    } catch (e) {} // eslint-disable-line no-empty
    return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.isInteger"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>isInteger ()](#apidoc.element.protobufjs.util.isInteger)
- description and source-code
```javascript
function isInteger() { [native code] }
```
- example usage
```shell
...
    } else {
switch (field.type) {
    case "int32":
    case "uint32":
    case "sint32":
    case "fixed32":
    case "sfixed32": gen
        ("if(!util.isInteger(%s))", ref)
            ("return%j", invalid(field, "integer"));
        break;
    case "int64":
    case "uint64":
    case "sint64":
    case "fixed64":
    case "sfixed64": gen
...
```

#### <a name="apidoc.element.protobufjs.util.isObject"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>isObject (value)](#apidoc.element.protobufjs.util.isObject)
- description and source-code
```javascript
function isObject(value) {
    return value && typeof value === "object";
}
```
- example usage
```shell
...
    for (var i = 0; i < /* initializes */ mtype.fieldsArray.length; ++i) {
var field = mtype._fieldsArray[i].resolve(),
    ref   = "m" + util.safeProp(field.name);

// map fields
if (field.map) { gen
    ("if(%s!=null){", ref) // !== undefined && !== null
        ("if(!util.isObject(%s))", ref)
            ("return%j", invalid(field, "object"))
        ("var k=Object.keys(%s)", ref)
        ("for(var i=0;i<k.length;++i){");
            genVerifyKey(gen, field, "k[i]");
            genVerifyValue(gen, field, i, ref + "[k[i]]")
        ("}")
    ("}");
...
```

#### <a name="apidoc.element.protobufjs.util.isSet"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>isSet (obj, prop)](#apidoc.element.protobufjs.util.isSet)
- description and source-code
```javascript
function isSet(obj, prop) {
    var value = obj[prop];
    if (value != null && obj.hasOwnProperty(prop)) // eslint-disable-line eqeqeq, no-prototype-builtins
        return typeof value !== "object" || (Array.isArray(value) ? value.length : Object.keys(value).length) > 0;
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.isString"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>isString (value)](#apidoc.element.protobufjs.util.isString)
- description and source-code
```javascript
function isString(value) {
    return typeof value === "string" || value instanceof String;
}
```
- example usage
```shell
...
            ("return%j", invalid(field, "number"));
        break;
    case "bool": gen
        ("if(typeof %s!==\"boolean\")", ref)
            ("return%j", invalid(field, "boolean"));
        break;
    case "string": gen
        ("if(!util.isString(%s))", ref)
            ("return%j", invalid(field, "string"));
        break;
    case "bytes": gen
        ("if(!(%s&&typeof %s.length===\"number\"||util.isString(%s)))", ref, ref, ref)
            ("return%j", invalid(field, "buffer"));
        break;
}
...
```

#### <a name="apidoc.element.protobufjs.util.isset"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>isset (obj, prop)](#apidoc.element.protobufjs.util.isset)
- description and source-code
```javascript
function isSet(obj, prop) {
    var value = obj[prop];
    if (value != null && obj.hasOwnProperty(prop)) // eslint-disable-line eqeqeq, no-prototype-builtins
        return typeof value !== "object" || (Array.isArray(value) ? value.length : Object.keys(value).length) > 0;
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.lazyResolve"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>lazyResolve (root, lazyTypes)](#apidoc.element.protobufjs.util.lazyResolve)
- description and source-code
```javascript
function lazyResolve(root, lazyTypes) {
    for (var i = 0; i < lazyTypes.length; ++i) {
        for (var keys = Object.keys(lazyTypes[i]), j = 0; j < keys.length; ++j) {
            var path = lazyTypes[i][keys[j]].split("."),
                ptr  = root;
            while (path.length)
                ptr = ptr[path.shift()];
            lazyTypes[i][keys[j]] = ptr;
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.lcFirst"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>lcFirst (str)](#apidoc.element.protobufjs.util.lcFirst)
- description and source-code
```javascript
function lcFirst(str) {
    return str.charAt(0).toLowerCase() + str.substring(1);
}
```
- example usage
```shell
...
    function parseGroup(parent, rule) {
var name = next();

/* istanbul ignore if */
if (!nameRe.test(name))
    throw illegal(name, "name");

var fieldName = util.lcFirst(name);
if (name === fieldName)
    name = util.ucFirst(name);
skip("=");
var id = parseId(next());
var type = new Type(name);
type.group = true;
var field = new Field(fieldName, id, name, rule);
...
```

#### <a name="apidoc.element.protobufjs.util.longFromHash"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>longFromHash (hash, unsigned)](#apidoc.element.protobufjs.util.longFromHash)
- description and source-code
```javascript
function longFromHash(hash, unsigned) {
    var bits = util.LongBits.fromHash(hash);
    if (util.Long)
        return util.Long.fromBits(bits.lo, bits.hi, unsigned);
    return bits.toNumber(Boolean(unsigned));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.longToHash"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>longToHash (value)](#apidoc.element.protobufjs.util.longToHash)
- description and source-code
```javascript
function longToHash(value) {
    return value
        ? util.LongBits.from(value).toHash()
        : util.LongBits.zeroHash;
}
```
- example usage
```shell
...
    ("r.skip().pos++") // assumes id 1 + key wireType
    ("if(%s===util.emptyObject)", ref)
        ("%s={}", ref)
    ("k=r.%s()", field.keyType)
    ("r.pos++"); // assumes id 2 + value wireType
if (types.long[field.keyType] !== undefined) {
    if (types.basic[type] === undefined) gen
    ("%s[typeof k===\"object\"?util.longToHash(k):k]=types[%d].decode(r,r.uint32())", ref, i); // can't be groups
    else gen
    ("%s[typeof k===\"object\"?util.longToHash(k):k]=r.%s()", ref, type);
} else {
    if (types.basic[type] === undefined) gen
    ("%s[k]=types[%d].decode(r,r.uint32())", ref, i); // can't be groups
    else gen
    ("%s[k]=r.%s()", ref, type);
...
```

#### <a name="apidoc.element.protobufjs.util.merge"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>merge (dst, src, ifNotSet)](#apidoc.element.protobufjs.util.merge)
- description and source-code
```javascript
function merge(dst, src, ifNotSet) { // used by converters
    for (var keys = Object.keys(src), i = 0; i < keys.length; ++i)
        if (dst[keys[i]] === undefined || !ifNotSet)
            dst[keys[i]] = src[keys[i]];
    return dst;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.newBuffer"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>newBuffer (sizeOrArray)](#apidoc.element.protobufjs.util.newBuffer)
- description and source-code
```javascript
function newBuffer(sizeOrArray) {
    /* istanbul ignore next */
    return typeof sizeOrArray === "number"
        ? util.Buffer
            ? util._Buffer_allocUnsafe(sizeOrArray)
            : new util.Array(sizeOrArray)
        : util.Buffer
            ? util._Buffer_from(sizeOrArray)
            : typeof Uint8Array === "undefined"
                ? sizeOrArray
                : new Uint8Array(sizeOrArray);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.newError"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>newError (name)](#apidoc.element.protobufjs.util.newError)
- description and source-code
```javascript
function newError(name) {

    function CustomError(message, properties) {

        if (!(this instanceof CustomError))
            return new CustomError(message, properties);

        // Error.call(this, message);
        // ^ just returns a new error instance because the ctor can be called as a function

        Object.defineProperty(this, "message", { get: function() { return message; } });

        /* istanbul ignore next */
        if (Error.captureStackTrace) // node
            Error.captureStackTrace(this, CustomError);
        else
            Object.defineProperty(this, "stack", { value: (new Error()).stack || "" });

        if (properties)
            merge(this, properties);
    }

    (CustomError.prototype = Object.create(Error.prototype)).constructor = CustomError;

    Object.defineProperty(CustomError.prototype, "name", { get: function() { return name; } });

    CustomError.prototype.toString = function toString() {
        return this.name + ": " + this.message;
    };

    return CustomError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.oneOfGetter"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>oneOfGetter (fieldNames)](#apidoc.element.protobufjs.util.oneOfGetter)
- description and source-code
```javascript
function getOneOf(fieldNames) {
    var fieldMap = {};
    for (var i = 0; i < fieldNames.length; ++i)
        fieldMap[fieldNames[i]] = 1;

    /**
     * @returns {string|undefined} Set field name, if any
     * @this Object
     * @ignore
     */
    return function() { // eslint-disable-line consistent-return
        for (var keys = Object.keys(this), i = keys.length - 1; i > -1; --i)
            if (fieldMap[keys[i]] === 1 && this[keys[i]] !== undefined && this[keys[i]] !== null)
                return keys[i];
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.oneOfSetter"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>oneOfSetter (fieldNames)](#apidoc.element.protobufjs.util.oneOfSetter)
- description and source-code
```javascript
function setOneOf(fieldNames) {

    /**
     * @param {string} name Field name
     * @returns {undefined}
     * @this Object
     * @ignore
     */
    return function(name) {
        for (var i = 0; i < fieldNames.length; ++i)
            if (fieldNames[i] !== name)
                delete this[fieldNames[i]];
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.pool"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>pool (alloc, slice, size)](#apidoc.element.protobufjs.util.pool)
- description and source-code
```javascript
function pool(alloc, slice, size) {
    var SIZE   = size || 8192;
    var MAX    = SIZE >>> 1;
    var slab   = null;
    var offset = SIZE;
    return function pool_alloc(size) {
        if (size < 1 || size > MAX)
            return alloc(size);
        if (offset + size > SIZE) {
            slab = alloc(SIZE);
            offset = 0;
        }
        var buf = slice.call(slab, offset, offset += size);
        if (offset & 7) // align to 32 bit
            offset = (offset | 7) + 1;
        return buf;
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.safeProp"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>safeProp (name)](#apidoc.element.protobufjs.util.safeProp)
- description and source-code
```javascript
function safeProp_dn(name) {
    return !/^[$\w]+$/.test(name) || exports.reserved(name)
        ? safeProp(name)
        : "." + name;
}
```
- example usage
```shell
...
    gen
("switch(t>>>3){");

    var i = 0;
    for (; i < /* initializes */ mtype.fieldsArray.length; ++i) {
var field = mtype._fieldsArray[i].resolve(),
    type  = field.resolvedType instanceof Enum ? "uint32" : field.type,
    ref   = "m" + util.safeProp(field.name); gen
    ("case %d:", field.id);

// Map fields
if (field.map) { gen
        ("r.skip().pos++") // assumes id 1 + key wireType
        ("if(%s===util.emptyObject)", ref)
            ("%s={}", ref)
...
```

#### <a name="apidoc.element.protobufjs.util.toArray"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>toArray (object)](#apidoc.element.protobufjs.util.toArray)
- description and source-code
```javascript
function toArray(object) {
    var array = [];
    if (object)
        for (var keys = Object.keys(object), i = 0; i < keys.length; ++i)
            array.push(object[keys[i]]);
    return array;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.ucFirst"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>ucFirst (str)](#apidoc.element.protobufjs.util.ucFirst)
- description and source-code
```javascript
function ucFirst(str) {
    return str.charAt(0).toUpperCase() + str.substring(1);
}
```
- example usage
```shell
...

/* istanbul ignore if */
if (!nameRe.test(name))
    throw illegal(name, "name");

var fieldName = util.lcFirst(name);
if (name === fieldName)
    name = util.ucFirst(name);
skip("=");
var id = parseId(next());
var type = new Type(name);
type.group = true;
var field = new Field(fieldName, id, name, rule);
field.filename = parse.filename;
ifBlock(type, function parseGroup_block(token) {
...
```



# <a name="apidoc.module.protobufjs.util.Buffer"></a>[module protobufjs.util.Buffer](#apidoc.module.protobufjs.util.Buffer)

#### <a name="apidoc.element.protobufjs.util.Buffer.Buffer"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.alloc"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>alloc (size, fill, encoding)](#apidoc.element.protobufjs.util.Buffer.alloc)
- description and source-code
```javascript
alloc = function (size, fill, encoding) {
  assertSize(size);
  if (size > 0 && fill !== undefined) {
    // Since we are filling anyway, don't zero fill initially.
    // Only pay attention to encoding if it's a string. This
    // prevents accidentally sending in a number that would
    // be interpretted as a start offset.
    if (typeof encoding !== 'string')
      encoding = undefined;
    return createUnsafeBuffer(size).fill(fill, encoding);
  }
  return new FastBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.allocUnsafe"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>allocUnsafe (size)](#apidoc.element.protobufjs.util.Buffer.allocUnsafe)
- description and source-code
```javascript
allocUnsafe = function (size) {
  assertSize(size);
  return allocate(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.allocUnsafeSlow"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>allocUnsafeSlow (size)](#apidoc.element.protobufjs.util.Buffer.allocUnsafeSlow)
- description and source-code
```javascript
allocUnsafeSlow = function (size) {
  assertSize(size);
  return createUnsafeBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.byteLength"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>byteLength (string, encoding)](#apidoc.element.protobufjs.util.Buffer.byteLength)
- description and source-code
```javascript
function byteLength(string, encoding) {
  if (typeof string !== 'string') {
    if (ArrayBuffer.isView(string) || isArrayBuffer(string) ||
        isSharedArrayBuffer(string)) {
      return string.byteLength;
    }

    string = '' + string;
  }

  var len = string.length;
  if (len === 0)
    return 0;

  // Use a for loop to avoid recursion
  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'ascii':
      case 'latin1':
      case 'binary':
        return len;

      case 'utf8':
      case 'utf-8':
      case undefined:
        return binding.byteLengthUtf8(string);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return len * 2;

      case 'hex':
        return len >>> 1;

      case 'base64':
        return base64ByteLength(string, len);

      default:
        // The C++ binding defaulted to UTF8, we should too.
        if (loweredCase)
          return binding.byteLengthUtf8(string);

        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.compare"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>compare (a, b)](#apidoc.element.protobufjs.util.Buffer.compare)
- description and source-code
```javascript
function compare(a, b) {
  if (!(a instanceof Buffer) ||
      !(b instanceof Buffer)) {
    throw new TypeError('Arguments must be Buffers');
  }

  if (a === b) {
    return 0;
  }

  return binding.compare(a, b);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.concat"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>concat (list, length)](#apidoc.element.protobufjs.util.Buffer.concat)
- description and source-code
```javascript
concat = function (list, length) {
  var i;
  if (!Array.isArray(list))
    throw new TypeError('"list" argument must be an Array of Buffers');

  if (list.length === 0)
    return new FastBuffer();

  if (length === undefined) {
    length = 0;
    for (i = 0; i < list.length; i++)
      length += list[i].length;
  } else {
    length = length >>> 0;
  }

  var buffer = Buffer.allocUnsafe(length);
  var pos = 0;
  for (i = 0; i < list.length; i++) {
    var buf = list[i];
    if (!Buffer.isBuffer(buf))
      throw new TypeError('"list" argument must be an Array of Buffers');
    buf.copy(buffer, pos);
    pos += buf.length;
  }

  // Note: 'length' is always equal to 'buffer.length' at this point
  if (pos < length) {
    // Zero-fill the remaining bytes if the specified 'length' was more than
    // the actual total length, i.e. if we have some remaining allocated bytes
    // there were not initialized.
    buffer.fill(0, pos, length);
  }

  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.from"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>from (value, encodingOrOffset, length)](#apidoc.element.protobufjs.util.Buffer.from)
- description and source-code
```javascript
from = function (value, encodingOrOffset, length) {
  if (typeof value === 'number')
    throw new TypeError('"value" argument must not be a number');

  if (isArrayBuffer(value) || isSharedArrayBuffer(value))
    return fromArrayBuffer(value, encodingOrOffset, length);

  if (typeof value === 'string')
    return fromString(value, encodingOrOffset);

  return fromObject(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.isBuffer"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>isBuffer (b)](#apidoc.element.protobufjs.util.Buffer.isBuffer)
- description and source-code
```javascript
function isBuffer(b) {
  return b instanceof Buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.isEncoding"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.</span>isEncoding (encoding)](#apidoc.element.protobufjs.util.Buffer.isEncoding)
- description and source-code
```javascript
isEncoding = function (encoding) {
  return typeof encoding === 'string' &&
         typeof internalUtil.normalizeEncoding(encoding) === 'string';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.Buffer.prototype"></a>[module protobufjs.util.Buffer.prototype](#apidoc.module.protobufjs.util.Buffer.prototype)

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.asciiSlice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>asciiSlice ()](#apidoc.element.protobufjs.util.Buffer.prototype.asciiSlice)
- description and source-code
```javascript
function asciiSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.asciiWrite"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>asciiWrite ()](#apidoc.element.protobufjs.util.Buffer.prototype.asciiWrite)
- description and source-code
```javascript
function asciiWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.base64Slice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>base64Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.base64Slice)
- description and source-code
```javascript
function base64Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.base64Write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>base64Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.base64Write)
- description and source-code
```javascript
function base64Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.compare"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.protobufjs.util.Buffer.prototype.compare)
- description and source-code
```javascript
function compare(target, start, end, thisStart, thisEnd) {

  if (!(target instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');
  if (arguments.length === 1)
    return compare_(this, target);

  if (start === undefined)
    start = 0;
  else if (start < 0)
    throw new RangeError('out of range index');
  else
    start >>>= 0;

  if (end === undefined)
    end = target.length;
  else if (end > target.length)
    throw new RangeError('out of range index');
  else
    end >>>= 0;

  if (thisStart === undefined)
    thisStart = 0;
  else if (thisStart < 0)
    throw new RangeError('out of range index');
  else
    thisStart >>>= 0;

  if (thisEnd === undefined)
    thisEnd = this.length;
  else if (thisEnd > this.length)
    throw new RangeError('out of range index');
  else
    thisEnd >>>= 0;

  if (thisStart >= thisEnd)
    return (start >= end ? 0 : -1);
  else if (start >= end)
    return 1;

  return compareOffset(this, target, start, thisStart, end, thisEnd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.copy"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>copy ()](#apidoc.element.protobufjs.util.Buffer.prototype.copy)
- description and source-code
```javascript
function copy() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.equals"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>equals (b)](#apidoc.element.protobufjs.util.Buffer.prototype.equals)
- description and source-code
```javascript
function equals(b) {
  if (!(b instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');

  if (this === b)
    return true;

  return binding.compare(this, b) === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.fill"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.fill)
- description and source-code
```javascript
function fill(val, start, end, encoding) {
  // Handle string cases:
  if (typeof val === 'string') {
    if (typeof start === 'string') {
      encoding = start;
      start = 0;
      end = this.length;
    } else if (typeof end === 'string') {
      encoding = end;
      end = this.length;
    }

    if (encoding !== undefined && typeof encoding !== 'string') {
      throw new TypeError('encoding must be a string');
    }
    var normalizedEncoding = internalUtil.normalizeEncoding(encoding);
    if (normalizedEncoding === undefined) {
      throw new TypeError('Unknown encoding: ' + encoding);
    }

    if (val.length === 0) {
      // Previously, if val === '', the Buffer would not fill,
      // which is rather surprising.
      val = 0;
    } else if (val.length === 1) {
      var code = val.charCodeAt(0);
      if ((normalizedEncoding === 'utf8' && code < 128) ||
          normalizedEncoding === 'latin1') {
        // Fast path: If 'val' fits into a single byte, use that numeric value.
        val = code;
      }
    }
  } else if (typeof val === 'number') {
    val = val & 255;
  }

  // Invalid ranges are not set to a default, so can range check early.
  if (start < 0 || end > this.length)
    throw new RangeError('Out of range index');

  if (end <= start)
    return this;

  start = start >>> 0;
  end = end === undefined ? this.length : end >>> 0;

  binding.fill(this, val, start, end, encoding);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.hexSlice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>hexSlice ()](#apidoc.element.protobufjs.util.Buffer.prototype.hexSlice)
- description and source-code
```javascript
function hexSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.hexWrite"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>hexWrite ()](#apidoc.element.protobufjs.util.Buffer.prototype.hexWrite)
- description and source-code
```javascript
function hexWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.includes"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.includes)
- description and source-code
```javascript
function includes(val, byteOffset, encoding) {
  return this.indexOf(val, byteOffset, encoding) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.indexOf)
- description and source-code
```javascript
function indexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, true);
}
```
- example usage
```shell
...

var fs   = require("fs"),
path = require("path");

// A profiling stub to measure encoding / decoding performance using benchmark data.

var commands = ["encode", "decode", "encode-browser", "decode-browser", "fromjson"];
if (commands.indexOf(process.argv[2]) < 0) { // 0: node, 1: prof.js
process.stderr.write("usage: " + path.basename(process.argv[1]) + " <" + commands.join("|") + "> [iterations=10000000]\n");
return;
}

// Spin up a node process with profiling enabled and process the generated log
if (process.execArgv.indexOf("--prof") < 0) {
process.stdout.write("cleaning up old logs ...\n");
...
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.inspect"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>inspect ()](#apidoc.element.protobufjs.util.Buffer.prototype.inspect)
- description and source-code
```javascript
function inspect() {
  var str = '';
  var max = exports.INSPECT_MAX_BYTES;
  if (this.length > 0) {
    str = this.toString('hex', 0, max).match(/.{2}/g).join(' ');
    if (this.length > max)
      str += ' ... ';
  }
  return '<' + this.constructor.name + ' ' + str + '>';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.latin1Slice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>latin1Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.latin1Slice)
- description and source-code
```javascript
function latin1Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.latin1Write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>latin1Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.latin1Write)
- description and source-code
```javascript
function latin1Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readDoubleBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readDoubleBE)
- description and source-code
```javascript
function readDoubleBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readDoubleLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readDoubleLE)
- description and source-code
```javascript
function readDoubleLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readFloatBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readFloatBE)
- description and source-code
```javascript
function readFloatBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readFloatLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readFloatLE)
- description and source-code
```javascript
function readFloatLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readInt16BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt16BE)
- description and source-code
```javascript
readInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset + 1] | (this[offset] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readInt16LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt16LE)
- description and source-code
```javascript
readInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset] | (this[offset + 1] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readInt32BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt32BE)
- description and source-code
```javascript
readInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] << 24) |
      (this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      (this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readInt32LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt32LE)
- description and source-code
```javascript
readInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16) |
      (this[offset + 3] << 24);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readInt8"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readInt8)
- description and source-code
```javascript
readInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  var val = this[offset];
  return !(val & 0x80) ? val : (0xff - val + 1) * -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readIntBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readIntBE)
- description and source-code
```javascript
readIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var i = byteLength;
  var mul = 1;
  var val = this[offset + --i];
  while (i > 0 && (mul *= 0x100))
    val += this[offset + --i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readIntLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readIntLE)
- description and source-code
```javascript
readIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUInt16BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt16BE)
- description and source-code
```javascript
readUInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return (this[offset] << 8) | this[offset + 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUInt16LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt16LE)
- description and source-code
```javascript
readUInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return this[offset] | (this[offset + 1] << 8);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUInt32BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt32BE)
- description and source-code
```javascript
readUInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] * 0x1000000) +
      ((this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUInt32LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt32LE)
- description and source-code
```javascript
readUInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return ((this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16)) +
      (this[offset + 3] * 0x1000000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUInt8"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUInt8)
- description and source-code
```javascript
readUInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  return this[offset];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUIntBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUIntBE)
- description and source-code
```javascript
readUIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset + --byteLength];
  var mul = 1;
  while (byteLength > 0 && (mul *= 0x100))
    val += this[offset + --byteLength] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.readUIntLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.readUIntLE)
- description and source-code
```javascript
readUIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.slice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>slice (start, end)](#apidoc.element.protobufjs.util.Buffer.prototype.slice)
- description and source-code
```javascript
function slice(start, end) {
  const srcLength = this.length;
  start = adjustOffset(start, srcLength);
  end = end !== undefined ? adjustOffset(end, srcLength) : srcLength;
  const newLength = end > start ? end - start : 0;
  return new FastBuffer(this.buffer, this.byteOffset + start, newLength);
}
```
- example usage
```shell
...
var child_process = require("child_process");
var logRe = /^isolate-[0-9A-F]+-v8\.log$/;
fs.readdirSync(process.cwd()).forEach(function readdirSync_it(file) {
    if (logRe.test(file))
        fs.unlink(file);
});
process.stdout.write("generating profile (may take a while) ...\n");
child_process.execSync("node --prof --trace-deopt " + process.execArgv.join(" ") + " " + process.argv.slice(1).join(" "), {
    cwd: process.cwd(),
    stdio: "inherit"
});
process.stdout.write("processing profile ...\n");
fs.readdirSync(process.cwd()).forEach(function readdirSync_it(file) {
    if (logRe.test(file)) {
        child_process.execSync("node --prof-process " + file, {
...
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.swap16"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap16 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap16)
- description and source-code
```javascript
function swap16() {
  // For Buffer.length < 128, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 2 !== 0)
    throw new RangeError('Buffer size must be a multiple of 16-bits');
  if (len < 128) {
    for (var i = 0; i < len; i += 2)
      swap(this, i, i + 1);
    return this;
  }
  return swap16n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.swap32"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap32 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap32)
- description and source-code
```javascript
function swap32() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 4 !== 0)
    throw new RangeError('Buffer size must be a multiple of 32-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 4) {
      swap(this, i, i + 3);
      swap(this, i + 1, i + 2);
    }
    return this;
  }
  return swap32n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.swap64"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>swap64 ()](#apidoc.element.protobufjs.util.Buffer.prototype.swap64)
- description and source-code
```javascript
function swap64() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 8 !== 0)
    throw new RangeError('Buffer size must be a multiple of 64-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 8) {
      swap(this, i, i + 7);
      swap(this, i + 1, i + 6);
      swap(this, i + 2, i + 5);
      swap(this, i + 3, i + 4);
    }
    return this;
  }
  return swap64n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>toJSON ()](#apidoc.element.protobufjs.util.Buffer.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  if (this.length) {
    const data = [];
    for (var i = 0; i < this.length; ++i)
      data[i] = this[i];
    return { type: 'Buffer', data };
  } else {
    return { type: 'Buffer', data: [] };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.toString"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>toString ()](#apidoc.element.protobufjs.util.Buffer.prototype.toString)
- description and source-code
```javascript
toString = function () {
  let result;
  if (arguments.length === 0) {
    result = this.utf8Slice(0, this.length);
  } else {
    result = slowToString.apply(this, arguments);
  }
  if (result === undefined)
    throw new Error('"toString()" failed');
  return result;
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.ucs2Slice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>ucs2Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.ucs2Slice)
- description and source-code
```javascript
function ucs2Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.ucs2Write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>ucs2Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.ucs2Write)
- description and source-code
```javascript
function ucs2Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.utf8Slice"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>utf8Slice ()](#apidoc.element.protobufjs.util.Buffer.prototype.utf8Slice)
- description and source-code
```javascript
function utf8Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.utf8Write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>utf8Write ()](#apidoc.element.protobufjs.util.Buffer.prototype.utf8Write)
- description and source-code
```javascript
function utf8Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.protobufjs.util.Buffer.prototype.write)
- description and source-code
```javascript
write = function (string, offset, length, encoding) {
  // Buffer#write(string);
  if (offset === undefined) {
    encoding = 'utf8';
    length = this.length;
    offset = 0;

  // Buffer#write(string, encoding)
  } else if (length === undefined && typeof offset === 'string') {
    encoding = offset;
    length = this.length;
    offset = 0;

  // Buffer#write(string, offset[, length][, encoding])
  } else if (isFinite(offset)) {
    offset = offset >>> 0;
    if (isFinite(length)) {
      length = length >>> 0;
      if (encoding === undefined)
        encoding = 'utf8';
    } else {
      encoding = length;
      length = undefined;
    }
  } else {
    // if someone is still calling the obsolete form of write(), tell them.
    // we don't want eg buf.write("foo", "utf8", 10) to silently turn into
    // buf.write("foo", "utf8"), so we can't ignore extra args
    throw new Error('Buffer.write(string, encoding, offset[, length]) ' +
                    'is no longer supported');
  }

  var remaining = this.length - offset;
  if (length === undefined || length > remaining)
    length = remaining;

  if (string.length > 0 && (length < 0 || offset < 0))
    throw new RangeError('Attempt to write outside buffer bounds');

  if (!encoding)
    encoding = 'utf8';

  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'hex':
        return this.hexWrite(string, offset, length);

      case 'utf8':
      case 'utf-8':
        return this.utf8Write(string, offset, length);

      case 'ascii':
        return this.asciiWrite(string, offset, length);

      case 'latin1':
      case 'binary':
        return this.latin1Write(string, offset, length);

      case 'base64':
        // Warning: maxLength not taken into account in base64Write
        return this.base64Write(string, offset, length);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return this.ucs2Write(string, offset, length);

      default:
        if (loweredCase)
          throw new TypeError('Unknown encoding: ' + encoding);
        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
...
var fs   = require("fs"),
path = require("path");

// A profiling stub to measure encoding / decoding performance using benchmark data.

var commands = ["encode", "decode", "encode-browser", "decode-browser", "fromjson"];
if (commands.indexOf(process.argv[2]) < 0) { // 0: node, 1: prof.js
process.stderr.write("usage: " + path.basename(process.argv[1]) + " <" + commands.join("|") + "> [iterations=10000000]\n");
return;
}

// Spin up a node process with profiling enabled and process the generated log
if (process.execArgv.indexOf("--prof") < 0) {
process.stdout.write("cleaning up old logs ...\n");
var child_process = require("child_process");
...
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleBE)
- description and source-code
```javascript
function writeDoubleBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleBE(this, val, offset);
  else
    binding.writeDoubleBE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeDoubleLE)
- description and source-code
```javascript
function writeDoubleLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleLE(this, val, offset);
  else
    binding.writeDoubleLE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeFloatBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeFloatBE)
- description and source-code
```javascript
function writeFloatBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatBE(this, val, offset);
  else
    binding.writeFloatBE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeFloatLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeFloatLE)
- description and source-code
```javascript
function writeFloatLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatLE(this, val, offset);
  else
    binding.writeFloatLE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeInt16BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt16BE)
- description and source-code
```javascript
writeInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeInt16LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt16LE)
- description and source-code
```javascript
writeInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeInt32BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt32BE)
- description and source-code
```javascript
writeInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeInt32LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt32LE)
- description and source-code
```javascript
writeInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  this[offset + 2] = (value >>> 16);
  this[offset + 3] = (value >>> 24);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeInt8"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeInt8)
- description and source-code
```javascript
writeInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0x7f, -0x80);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeIntBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeIntBE)
- description and source-code
```javascript
writeIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = byteLength - 1;
  var mul = 1;
  var sub = 0;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i + 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeIntLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeIntLE)
- description and source-code
```javascript
writeIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = 0;
  var mul = 1;
  var sub = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i - 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16BE)
- description and source-code
```javascript
writeUInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt16LE)
- description and source-code
```javascript
writeUInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32BE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32BE)
- description and source-code
```javascript
writeUInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32LE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt32LE)
- description and source-code
```javascript
writeUInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset + 3] = (value >>> 24);
  this[offset + 2] = (value >>> 16);
  this[offset + 1] = (value >>> 8);
  this[offset] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUInt8"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUInt8)
- description and source-code
```javascript
writeUInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0xff, 0);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUIntBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUIntBE)
- description and source-code
```javascript
writeUIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var i = byteLength - 1;
  var mul = 1;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Buffer.prototype.writeUIntLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Buffer.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.protobufjs.util.Buffer.prototype.writeUIntLE)
- description and source-code
```javascript
writeUIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var mul = 1;
  var i = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.EventEmitter"></a>[module protobufjs.util.EventEmitter](#apidoc.module.protobufjs.util.EventEmitter)

#### <a name="apidoc.element.protobufjs.util.EventEmitter.EventEmitter"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>EventEmitter ()](#apidoc.element.protobufjs.util.EventEmitter.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {

    /**
     * Registered listeners.
     * @type {Object.<string,*>}
     * @private
     */
    this._listeners = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.EventEmitter.prototype"></a>[module protobufjs.util.EventEmitter.prototype](#apidoc.module.protobufjs.util.EventEmitter.prototype)

#### <a name="apidoc.element.protobufjs.util.EventEmitter.prototype.emit"></a>[function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>emit (evt)](#apidoc.element.protobufjs.util.EventEmitter.prototype.emit)
- description and source-code
```javascript
function emit(evt) {
    var listeners = this._listeners[evt];
    if (listeners) {
        var args = [],
            i = 1;
        for (; i < arguments.length;)
            args.push(arguments[i++]);
        for (i = 0; i < listeners.length;)
            listeners[i].fn.apply(listeners[i++].ctx, args);
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.EventEmitter.prototype.off"></a>[function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>off (evt, fn)](#apidoc.element.protobufjs.util.EventEmitter.prototype.off)
- description and source-code
```javascript
function off(evt, fn) {
    if (evt === undefined)
        this._listeners = {};
    else {
        if (fn === undefined)
            this._listeners[evt] = [];
        else {
            var listeners = this._listeners[evt];
            for (var i = 0; i < listeners.length;)
                if (listeners[i].fn === fn)
                    listeners.splice(i, 1);
                else
                    ++i;
        }
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.EventEmitter.prototype.on"></a>[function <span class="apidocSignatureSpan">protobufjs.util.EventEmitter.prototype.</span>on (evt, fn, ctx)](#apidoc.element.protobufjs.util.EventEmitter.prototype.on)
- description and source-code
```javascript
function on(evt, fn, ctx) {
    (this._listeners[evt] || (this._listeners[evt] = [])).push({
        fn  : fn,
        ctx : ctx || this
    });
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.Long"></a>[module protobufjs.util.Long](#apidoc.module.protobufjs.util.Long)

#### <a name="apidoc.element.protobufjs.util.Long.Long"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>Long (low, high, unsigned)](#apidoc.element.protobufjs.util.Long.Long)
- description and source-code
```javascript
function Long(low, high, unsigned) {

    /**
     * The low 32 bits as a signed value.
     * @type {number}
     */
    this.low = low | 0;

    /**
     * The high 32 bits as a signed value.
     * @type {number}
     */
    this.high = high | 0;

    /**
     * Whether unsigned or not.
     * @type {boolean}
     */
    this.unsigned = !!unsigned;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.fromBits"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromBits (lowBits, highBits, unsigned)](#apidoc.element.protobufjs.util.Long.fromBits)
- description and source-code
```javascript
function fromBits(lowBits, highBits, unsigned) {
    return new Long(lowBits, highBits, unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.fromInt"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromInt (value, unsigned)](#apidoc.element.protobufjs.util.Long.fromInt)
- description and source-code
```javascript
function fromInt(value, unsigned) {
    var obj, cachedObj, cache;
    if (unsigned) {
        value >>>= 0;
        if (cache = (0 <= value && value < 256)) {
            cachedObj = UINT_CACHE[value];
            if (cachedObj)
                return cachedObj;
        }
        obj = fromBits(value, (value | 0) < 0 ? -1 : 0, true);
        if (cache)
            UINT_CACHE[value] = obj;
        return obj;
    } else {
        value |= 0;
        if (cache = (-128 <= value && value < 128)) {
            cachedObj = INT_CACHE[value];
            if (cachedObj)
                return cachedObj;
        }
        obj = fromBits(value, value < 0 ? -1 : 0, false);
        if (cache)
            INT_CACHE[value] = obj;
        return obj;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.fromNumber"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromNumber (value, unsigned)](#apidoc.element.protobufjs.util.Long.fromNumber)
- description and source-code
```javascript
function fromNumber(value, unsigned) {
    if (isNaN(value) || !isFinite(value))
        return unsigned ? UZERO : ZERO;
    if (unsigned) {
        if (value < 0)
            return UZERO;
        if (value >= TWO_PWR_64_DBL)
            return MAX_UNSIGNED_VALUE;
    } else {
        if (value <= -TWO_PWR_63_DBL)
            return MIN_VALUE;
        if (value + 1 >= TWO_PWR_63_DBL)
            return MAX_VALUE;
    }
    if (value < 0)
        return fromNumber(-value, unsigned).neg();
    return fromBits((value % TWO_PWR_32_DBL) | 0, (value / TWO_PWR_32_DBL) | 0, unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.fromString"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromString (str, unsigned, radix)](#apidoc.element.protobufjs.util.Long.fromString)
- description and source-code
```javascript
function fromString(str, unsigned, radix) {
    if (str.length === 0)
        throw Error('empty string');
    if (str === "NaN" || str === "Infinity" || str === "+Infinity" || str === "-Infinity")
        return ZERO;
    if (typeof unsigned === 'number') {
        // For goog.math.long compatibility
        radix = unsigned,
        unsigned = false;
    } else {
        unsigned = !! unsigned;
    }
    radix = radix || 10;
    if (radix < 2 || 36 < radix)
        throw RangeError('radix');

    var p;
    if ((p = str.indexOf('-')) > 0)
        throw Error('interior hyphen');
    else if (p === 0) {
        return fromString(str.substring(1), unsigned, radix).neg();
    }

    // Do several (8) digits each time through the loop, so as to
    // minimize the calls to the very expensive emulated div.
    var radixToPower = fromNumber(pow_dbl(radix, 8));

    var result = ZERO;
    for (var i = 0; i < str.length; i += 8) {
        var size = Math.min(8, str.length - i),
            value = parseInt(str.substring(i, i + size), radix);
        if (size < 8) {
            var power = fromNumber(pow_dbl(radix, size));
            result = result.mul(power).add(fromNumber(value));
        } else {
            result = result.mul(radixToPower);
            result = result.add(fromNumber(value));
        }
    }
    result.unsigned = unsigned;
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.fromValue"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>fromValue (val)](#apidoc.element.protobufjs.util.Long.fromValue)
- description and source-code
```javascript
function fromValue(val) {
    if (val /* is compatible */ instanceof Long)
        return val;
    if (typeof val === 'number')
        return fromNumber(val);
    if (typeof val === 'string')
        return fromString(val);
    // Throws for non-objects, converts non-instanceof Long:
    return fromBits(val.low, val.high, val.unsigned);
}
```
- example usage
```shell
...
* Calling 'Message.verify' with any object returns 'null' if the object can be encoded as-is and otherwise the error as a string
.
* Calling 'Message.create' or 'Message.encode' must be called with a valid message.
* Calling 'Message.fromObject' with any object naively converts all values to the optimal JS type.

| Field type | Expected JS type (create, encode) | Naive conversion (fromObject)
|------------|-----------------------------------|------------------------------
| s-/u-/int32<br />s-/fixed32 | 'Number' (32 bit integer) | 'value | 0' if signed<br /> 'value >>> 0' if unsigned
| s-/u-/int64<br />s-/fixed64 | 'Long'-like (optimal)<br />'Number' (53 bit integer) | 'Long.fromValue(value)' with long.js<br />'
parseInt(value, 10)' otherwise
| float<br />double | 'Number' | 'Number(value)'
| bool | 'Boolean' | 'Boolean(value)'
| string | 'String' | 'String(value)'
| bytes | 'Uint8Array' (optimal)<br />'Buffer' (optimal under node)<br />'Array.<Number>' (8 bit integers)<br />'String' (base64
) | 'base64.decode(value)' if a String<br />'Object' with non-zero '.length' is kept
| enum | 'Number' (32 bit integer) | Looks up the numeric id if a string
| message | Valid message | 'Message.fromObject(value)'
...
```

#### <a name="apidoc.element.protobufjs.util.Long.isLong"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.</span>isLong (obj)](#apidoc.element.protobufjs.util.Long.isLong)
- description and source-code
```javascript
function isLong(obj) {
    return (obj && obj["__isLong__"]) === true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.Long.prototype"></a>[module protobufjs.util.Long.prototype](#apidoc.module.protobufjs.util.Long.prototype)

#### <a name="apidoc.element.protobufjs.util.Long.prototype.add"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>add (addend)](#apidoc.element.protobufjs.util.Long.prototype.add)
- description and source-code
```javascript
function add(addend) {
    if (!isLong(addend))
        addend = fromValue(addend);

    // Divide each number into 4 chunks of 16 bits, and then sum the chunks.

    var a48 = this.high >>> 16;
    var a32 = this.high & 0xFFFF;
    var a16 = this.low >>> 16;
    var a00 = this.low & 0xFFFF;

    var b48 = addend.high >>> 16;
    var b32 = addend.high & 0xFFFF;
    var b16 = addend.low >>> 16;
    var b00 = addend.low & 0xFFFF;

    var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
    c00 += a00 + b00;
    c16 += c00 >>> 16;
    c00 &= 0xFFFF;
    c16 += a16 + b16;
    c32 += c16 >>> 16;
    c16 &= 0xFFFF;
    c32 += a32 + b32;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c48 += a48 + b48;
    c48 &= 0xFFFF;
    return fromBits((c16 << 16) | c00, (c48 << 16) | c32, this.unsigned);
}
```
- example usage
```shell
...

'''js
...
var Root  = protobuf.Root,
    Type  = protobuf.Type,
    Field = protobuf.Field;

var AwesomeMessage = new Type("AwesomeMessage").add(new Field("awesomeField", 1, "string"));

var root = new Root().define("awesomepackage").add(AwesomeMessage);

// Continue at "Create a new message" above
...
'''
...
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.and"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>and (other)](#apidoc.element.protobufjs.util.Long.prototype.and)
- description and source-code
```javascript
function and(other) {
    if (!isLong(other))
        other = fromValue(other);
    return fromBits(this.low & other.low, this.high & other.high, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.comp"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>comp (other)](#apidoc.element.protobufjs.util.Long.prototype.comp)
- description and source-code
```javascript
function compare(other) {
    if (!isLong(other))
        other = fromValue(other);
    if (this.eq(other))
        return 0;
    var thisNeg = this.isNegative(),
        otherNeg = other.isNegative();
    if (thisNeg && !otherNeg)
        return -1;
    if (!thisNeg && otherNeg)
        return 1;
    // At this point the sign bits are the same
    if (!this.unsigned)
        return this.sub(other).isNegative() ? -1 : 1;
    // Both are positive if at least one is unsigned
    return (other.high >>> 0) > (this.high >>> 0) || (other.high === this.high && (other.low >>> 0) > (this.low >>> 0)) ? -1 : 1
;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.compare"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>compare (other)](#apidoc.element.protobufjs.util.Long.prototype.compare)
- description and source-code
```javascript
function compare(other) {
    if (!isLong(other))
        other = fromValue(other);
    if (this.eq(other))
        return 0;
    var thisNeg = this.isNegative(),
        otherNeg = other.isNegative();
    if (thisNeg && !otherNeg)
        return -1;
    if (!thisNeg && otherNeg)
        return 1;
    // At this point the sign bits are the same
    if (!this.unsigned)
        return this.sub(other).isNegative() ? -1 : 1;
    // Both are positive if at least one is unsigned
    return (other.high >>> 0) > (this.high >>> 0) || (other.high === this.high && (other.low >>> 0) > (this.low >>> 0)) ? -1 : 1
;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.div"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>div (divisor)](#apidoc.element.protobufjs.util.Long.prototype.div)
- description and source-code
```javascript
function divide(divisor) {
    if (!isLong(divisor))
        divisor = fromValue(divisor);
    if (divisor.isZero())
        throw Error('division by zero');
    if (this.isZero())
        return this.unsigned ? UZERO : ZERO;
    var approx, rem, res;
    if (!this.unsigned) {
        // This section is only relevant for signed longs and is derived from the
        // closure library as a whole.
        if (this.eq(MIN_VALUE)) {
            if (divisor.eq(ONE) || divisor.eq(NEG_ONE))
                return MIN_VALUE;  // recall that -MIN_VALUE == MIN_VALUE
            else if (divisor.eq(MIN_VALUE))
                return ONE;
            else {
                // At this point, we have |other| >= 2, so |this/other| < |MIN_VALUE|.
                var halfThis = this.shr(1);
                approx = halfThis.div(divisor).shl(1);
                if (approx.eq(ZERO)) {
                    return divisor.isNegative() ? ONE : NEG_ONE;
                } else {
                    rem = this.sub(divisor.mul(approx));
                    res = approx.add(rem.div(divisor));
                    return res;
                }
            }
        } else if (divisor.eq(MIN_VALUE))
            return this.unsigned ? UZERO : ZERO;
        if (this.isNegative()) {
            if (divisor.isNegative())
                return this.neg().div(divisor.neg());
            return this.neg().div(divisor).neg();
        } else if (divisor.isNegative())
            return this.div(divisor.neg()).neg();
        res = ZERO;
    } else {
        // The algorithm below has not been made for unsigned longs. It's therefore
        // required to take special care of the MSB prior to running it.
        if (!divisor.unsigned)
            divisor = divisor.toUnsigned();
        if (divisor.gt(this))
            return UZERO;
        if (divisor.gt(this.shru(1))) // 15 >>> 1 = 7 ; with divisor = 8 ; true
            return UONE;
        res = UZERO;
    }

    // Repeat the following until the remainder is less than other:  find a
    // floating-point that approximates remainder / other *from below*, add this
    // into the result, and subtract it from the remainder.  It is critical that
    // the approximate value is less than or equal to the real value so that the
    // remainder never becomes negative.
    rem = this;
    while (rem.gte(divisor)) {
        // Approximate the result of division. This may be a little greater or
        // smaller than the actual value.
        approx = Math.max(1, Math.floor(rem.toNumber() / divisor.toNumber()));

        // We will tweak the approximate result by changing it in the 48-th digit or
        // the smallest non-fractional digit, whichever is larger.
        var log2 = Math.ceil(Math.log(approx) / Math.LN2),
            delta = (log2 <= 48) ? 1 : pow_dbl(2, log2 - 48),

        // Decrease the approximation until it is smaller than the remainder.  Note
        // that if it is too large, the product overflows and is negative.
            approxRes = fromNumber(approx),
            approxRem = approxRes.mul(divisor);
        while (approxRem.isNegative() || approxRem.gt(rem)) {
            approx -= delta;
            approxRes = fromNumber(approx, this.unsigned);
            approxRem = approxRes.mul(divisor);
        }

        // We know the answer can't be zero... and actually, zero would cause
        // infinite recursion since we would make no progress.
        if (approxRes.isZero())
            approxRes = ONE;

        res = res.add(approxRes);
        rem = rem.sub(approxRem);
    }
    return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.divide"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>divide (divisor)](#apidoc.element.protobufjs.util.Long.prototype.divide)
- description and source-code
```javascript
function divide(divisor) {
    if (!isLong(divisor))
        divisor = fromValue(divisor);
    if (divisor.isZero())
        throw Error('division by zero');
    if (this.isZero())
        return this.unsigned ? UZERO : ZERO;
    var approx, rem, res;
    if (!this.unsigned) {
        // This section is only relevant for signed longs and is derived from the
        // closure library as a whole.
        if (this.eq(MIN_VALUE)) {
            if (divisor.eq(ONE) || divisor.eq(NEG_ONE))
                return MIN_VALUE;  // recall that -MIN_VALUE == MIN_VALUE
            else if (divisor.eq(MIN_VALUE))
                return ONE;
            else {
                // At this point, we have |other| >= 2, so |this/other| < |MIN_VALUE|.
                var halfThis = this.shr(1);
                approx = halfThis.div(divisor).shl(1);
                if (approx.eq(ZERO)) {
                    return divisor.isNegative() ? ONE : NEG_ONE;
                } else {
                    rem = this.sub(divisor.mul(approx));
                    res = approx.add(rem.div(divisor));
                    return res;
                }
            }
        } else if (divisor.eq(MIN_VALUE))
            return this.unsigned ? UZERO : ZERO;
        if (this.isNegative()) {
            if (divisor.isNegative())
                return this.neg().div(divisor.neg());
            return this.neg().div(divisor).neg();
        } else if (divisor.isNegative())
            return this.div(divisor.neg()).neg();
        res = ZERO;
    } else {
        // The algorithm below has not been made for unsigned longs. It's therefore
        // required to take special care of the MSB prior to running it.
        if (!divisor.unsigned)
            divisor = divisor.toUnsigned();
        if (divisor.gt(this))
            return UZERO;
        if (divisor.gt(this.shru(1))) // 15 >>> 1 = 7 ; with divisor = 8 ; true
            return UONE;
        res = UZERO;
    }

    // Repeat the following until the remainder is less than other:  find a
    // floating-point that approximates remainder / other *from below*, add this
    // into the result, and subtract it from the remainder.  It is critical that
    // the approximate value is less than or equal to the real value so that the
    // remainder never becomes negative.
    rem = this;
    while (rem.gte(divisor)) {
        // Approximate the result of division. This may be a little greater or
        // smaller than the actual value.
        approx = Math.max(1, Math.floor(rem.toNumber() / divisor.toNumber()));

        // We will tweak the approximate result by changing it in the 48-th digit or
        // the smallest non-fractional digit, whichever is larger.
        var log2 = Math.ceil(Math.log(approx) / Math.LN2),
            delta = (log2 <= 48) ? 1 : pow_dbl(2, log2 - 48),

        // Decrease the approximation until it is smaller than the remainder.  Note
        // that if it is too large, the product overflows and is negative.
            approxRes = fromNumber(approx),
            approxRem = approxRes.mul(divisor);
        while (approxRem.isNegative() || approxRem.gt(rem)) {
            approx -= delta;
            approxRes = fromNumber(approx, this.unsigned);
            approxRem = approxRes.mul(divisor);
        }

        // We know the answer can't be zero... and actually, zero would cause
        // infinite recursion since we would make no progress.
        if (approxRes.isZero())
            approxRes = ONE;

        res = res.add(approxRes);
        rem = rem.sub(approxRem);
    }
    return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.eq"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>eq (other)](#apidoc.element.protobufjs.util.Long.prototype.eq)
- description and source-code
```javascript
function equals(other) {
    if (!isLong(other))
        other = fromValue(other);
    if (this.unsigned !== other.unsigned && (this.high >>> 31) === 1 && (other.high >>> 31) === 1)
        return false;
    return this.high === other.high && this.low === other.low;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.equals"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>equals (other)](#apidoc.element.protobufjs.util.Long.prototype.equals)
- description and source-code
```javascript
function equals(other) {
    if (!isLong(other))
        other = fromValue(other);
    if (this.unsigned !== other.unsigned && (this.high >>> 31) === 1 && (other.high >>> 31) === 1)
        return false;
    return this.high === other.high && this.low === other.low;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.getHighBits"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getHighBits ()](#apidoc.element.protobufjs.util.Long.prototype.getHighBits)
- description and source-code
```javascript
function getHighBits() {
    return this.high;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.getHighBitsUnsigned"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getHighBitsUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.getHighBitsUnsigned)
- description and source-code
```javascript
function getHighBitsUnsigned() {
    return this.high >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.getLowBits"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getLowBits ()](#apidoc.element.protobufjs.util.Long.prototype.getLowBits)
- description and source-code
```javascript
function getLowBits() {
    return this.low;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.getLowBitsUnsigned"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.getLowBitsUnsigned)
- description and source-code
```javascript
function getLowBitsUnsigned() {
    return this.low >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.getNumBitsAbs"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>getNumBitsAbs ()](#apidoc.element.protobufjs.util.Long.prototype.getNumBitsAbs)
- description and source-code
```javascript
function getNumBitsAbs() {
    if (this.isNegative()) // Unsigned Longs are never negative
        return this.eq(MIN_VALUE) ? 64 : this.neg().getNumBitsAbs();
    var val = this.high != 0 ? this.high : this.low;
    for (var bit = 31; bit > 0; bit--)
        if ((val & (1 << bit)) != 0)
            break;
    return this.high != 0 ? bit + 33 : bit + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.greaterThan"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>greaterThan (other)](#apidoc.element.protobufjs.util.Long.prototype.greaterThan)
- description and source-code
```javascript
function greaterThan(other) {
    return this.comp(/* validates */ other) > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.greaterThanOrEqual"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.protobufjs.util.Long.prototype.greaterThanOrEqual)
- description and source-code
```javascript
function greaterThanOrEqual(other) {
    return this.comp(/* validates */ other) >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.gt"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>gt (other)](#apidoc.element.protobufjs.util.Long.prototype.gt)
- description and source-code
```javascript
function greaterThan(other) {
    return this.comp(/* validates */ other) > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.gte"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>gte (other)](#apidoc.element.protobufjs.util.Long.prototype.gte)
- description and source-code
```javascript
function greaterThanOrEqual(other) {
    return this.comp(/* validates */ other) >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.isEven"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isEven ()](#apidoc.element.protobufjs.util.Long.prototype.isEven)
- description and source-code
```javascript
function isEven() {
    return (this.low & 1) === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.isNegative"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isNegative ()](#apidoc.element.protobufjs.util.Long.prototype.isNegative)
- description and source-code
```javascript
function isNegative() {
    return !this.unsigned && this.high < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.isOdd"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isOdd ()](#apidoc.element.protobufjs.util.Long.prototype.isOdd)
- description and source-code
```javascript
function isOdd() {
    return (this.low & 1) === 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.isPositive"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isPositive ()](#apidoc.element.protobufjs.util.Long.prototype.isPositive)
- description and source-code
```javascript
function isPositive() {
    return this.unsigned || this.high >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.isZero"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>isZero ()](#apidoc.element.protobufjs.util.Long.prototype.isZero)
- description and source-code
```javascript
function isZero() {
    return this.high === 0 && this.low === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.lessThan"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lessThan (other)](#apidoc.element.protobufjs.util.Long.prototype.lessThan)
- description and source-code
```javascript
function lessThan(other) {
    return this.comp(/* validates */ other) < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.lessThanOrEqual"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lessThanOrEqual (other)](#apidoc.element.protobufjs.util.Long.prototype.lessThanOrEqual)
- description and source-code
```javascript
function lessThanOrEqual(other) {
    return this.comp(/* validates */ other) <= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.lt"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lt (other)](#apidoc.element.protobufjs.util.Long.prototype.lt)
- description and source-code
```javascript
function lessThan(other) {
    return this.comp(/* validates */ other) < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.lte"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>lte (other)](#apidoc.element.protobufjs.util.Long.prototype.lte)
- description and source-code
```javascript
function lessThanOrEqual(other) {
    return this.comp(/* validates */ other) <= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.mod"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>mod (divisor)](#apidoc.element.protobufjs.util.Long.prototype.mod)
- description and source-code
```javascript
function modulo(divisor) {
    if (!isLong(divisor))
        divisor = fromValue(divisor);
    return this.sub(this.div(divisor).mul(divisor));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.modulo"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>modulo (divisor)](#apidoc.element.protobufjs.util.Long.prototype.modulo)
- description and source-code
```javascript
function modulo(divisor) {
    if (!isLong(divisor))
        divisor = fromValue(divisor);
    return this.sub(this.div(divisor).mul(divisor));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.mul"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>mul (multiplier)](#apidoc.element.protobufjs.util.Long.prototype.mul)
- description and source-code
```javascript
function multiply(multiplier) {
    if (this.isZero())
        return ZERO;
    if (!isLong(multiplier))
        multiplier = fromValue(multiplier);
    if (multiplier.isZero())
        return ZERO;
    if (this.eq(MIN_VALUE))
        return multiplier.isOdd() ? MIN_VALUE : ZERO;
    if (multiplier.eq(MIN_VALUE))
        return this.isOdd() ? MIN_VALUE : ZERO;

    if (this.isNegative()) {
        if (multiplier.isNegative())
            return this.neg().mul(multiplier.neg());
        else
            return this.neg().mul(multiplier).neg();
    } else if (multiplier.isNegative())
        return this.mul(multiplier.neg()).neg();

    // If both longs are small, use float multiplication
    if (this.lt(TWO_PWR_24) && multiplier.lt(TWO_PWR_24))
        return fromNumber(this.toNumber() * multiplier.toNumber(), this.unsigned);

    // Divide each long into 4 chunks of 16 bits, and then add up 4x4 products.
    // We can skip products that would overflow.

    var a48 = this.high >>> 16;
    var a32 = this.high & 0xFFFF;
    var a16 = this.low >>> 16;
    var a00 = this.low & 0xFFFF;

    var b48 = multiplier.high >>> 16;
    var b32 = multiplier.high & 0xFFFF;
    var b16 = multiplier.low >>> 16;
    var b00 = multiplier.low & 0xFFFF;

    var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
    c00 += a00 * b00;
    c16 += c00 >>> 16;
    c00 &= 0xFFFF;
    c16 += a16 * b00;
    c32 += c16 >>> 16;
    c16 &= 0xFFFF;
    c16 += a00 * b16;
    c32 += c16 >>> 16;
    c16 &= 0xFFFF;
    c32 += a32 * b00;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c32 += a16 * b16;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c32 += a00 * b32;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c48 += a48 * b00 + a32 * b16 + a16 * b32 + a00 * b48;
    c48 &= 0xFFFF;
    return fromBits((c16 << 16) | c00, (c48 << 16) | c32, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.multiply"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>multiply (multiplier)](#apidoc.element.protobufjs.util.Long.prototype.multiply)
- description and source-code
```javascript
function multiply(multiplier) {
    if (this.isZero())
        return ZERO;
    if (!isLong(multiplier))
        multiplier = fromValue(multiplier);
    if (multiplier.isZero())
        return ZERO;
    if (this.eq(MIN_VALUE))
        return multiplier.isOdd() ? MIN_VALUE : ZERO;
    if (multiplier.eq(MIN_VALUE))
        return this.isOdd() ? MIN_VALUE : ZERO;

    if (this.isNegative()) {
        if (multiplier.isNegative())
            return this.neg().mul(multiplier.neg());
        else
            return this.neg().mul(multiplier).neg();
    } else if (multiplier.isNegative())
        return this.mul(multiplier.neg()).neg();

    // If both longs are small, use float multiplication
    if (this.lt(TWO_PWR_24) && multiplier.lt(TWO_PWR_24))
        return fromNumber(this.toNumber() * multiplier.toNumber(), this.unsigned);

    // Divide each long into 4 chunks of 16 bits, and then add up 4x4 products.
    // We can skip products that would overflow.

    var a48 = this.high >>> 16;
    var a32 = this.high & 0xFFFF;
    var a16 = this.low >>> 16;
    var a00 = this.low & 0xFFFF;

    var b48 = multiplier.high >>> 16;
    var b32 = multiplier.high & 0xFFFF;
    var b16 = multiplier.low >>> 16;
    var b00 = multiplier.low & 0xFFFF;

    var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
    c00 += a00 * b00;
    c16 += c00 >>> 16;
    c00 &= 0xFFFF;
    c16 += a16 * b00;
    c32 += c16 >>> 16;
    c16 &= 0xFFFF;
    c16 += a00 * b16;
    c32 += c16 >>> 16;
    c16 &= 0xFFFF;
    c32 += a32 * b00;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c32 += a16 * b16;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c32 += a00 * b32;
    c48 += c32 >>> 16;
    c32 &= 0xFFFF;
    c48 += a48 * b00 + a32 * b16 + a16 * b32 + a00 * b48;
    c48 &= 0xFFFF;
    return fromBits((c16 << 16) | c00, (c48 << 16) | c32, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.neg"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>neg ()](#apidoc.element.protobufjs.util.Long.prototype.neg)
- description and source-code
```javascript
function negate() {
    if (!this.unsigned && this.eq(MIN_VALUE))
        return MIN_VALUE;
    return this.not().add(ONE);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.negate"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>negate ()](#apidoc.element.protobufjs.util.Long.prototype.negate)
- description and source-code
```javascript
function negate() {
    if (!this.unsigned && this.eq(MIN_VALUE))
        return MIN_VALUE;
    return this.not().add(ONE);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.neq"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>neq (other)](#apidoc.element.protobufjs.util.Long.prototype.neq)
- description and source-code
```javascript
function notEquals(other) {
    return !this.eq(/* validates */ other);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.not"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>not ()](#apidoc.element.protobufjs.util.Long.prototype.not)
- description and source-code
```javascript
function not() {
    return fromBits(~this.low, ~this.high, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.notEquals"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>notEquals (other)](#apidoc.element.protobufjs.util.Long.prototype.notEquals)
- description and source-code
```javascript
function notEquals(other) {
    return !this.eq(/* validates */ other);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.or"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>or (other)](#apidoc.element.protobufjs.util.Long.prototype.or)
- description and source-code
```javascript
function or(other) {
    if (!isLong(other))
        other = fromValue(other);
    return fromBits(this.low | other.low, this.high | other.high, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shiftLeft"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftLeft (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftLeft)
- description and source-code
```javascript
function shiftLeft(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    if ((numBits &= 63) === 0)
        return this;
    else if (numBits < 32)
        return fromBits(this.low << numBits, (this.high << numBits) | (this.low >>> (32 - numBits)), this.unsigned);
    else
        return fromBits(0, this.low << (numBits - 32), this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shiftRight"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftRight (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftRight)
- description and source-code
```javascript
function shiftRight(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    if ((numBits &= 63) === 0)
        return this;
    else if (numBits < 32)
        return fromBits((this.low >>> numBits) | (this.high << (32 - numBits)), this.high >> numBits, this.unsigned);
    else
        return fromBits(this.high >> (numBits - 32), this.high >= 0 ? 0 : -1, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shiftRightUnsigned"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shiftRightUnsigned)
- description and source-code
```javascript
function shiftRightUnsigned(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    numBits &= 63;
    if (numBits === 0)
        return this;
    else {
        var high = this.high;
        if (numBits < 32) {
            var low = this.low;
            return fromBits((low >>> numBits) | (high << (32 - numBits)), high >>> numBits, this.unsigned);
        } else if (numBits === 32)
            return fromBits(high, 0, this.unsigned);
        else
            return fromBits(high >>> (numBits - 32), 0, this.unsigned);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shl"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shl (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shl)
- description and source-code
```javascript
function shiftLeft(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    if ((numBits &= 63) === 0)
        return this;
    else if (numBits < 32)
        return fromBits(this.low << numBits, (this.high << numBits) | (this.low >>> (32 - numBits)), this.unsigned);
    else
        return fromBits(0, this.low << (numBits - 32), this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shr"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shr (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shr)
- description and source-code
```javascript
function shiftRight(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    if ((numBits &= 63) === 0)
        return this;
    else if (numBits < 32)
        return fromBits((this.low >>> numBits) | (this.high << (32 - numBits)), this.high >> numBits, this.unsigned);
    else
        return fromBits(this.high >> (numBits - 32), this.high >= 0 ? 0 : -1, this.unsigned);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.shru"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>shru (numBits)](#apidoc.element.protobufjs.util.Long.prototype.shru)
- description and source-code
```javascript
function shiftRightUnsigned(numBits) {
    if (isLong(numBits))
        numBits = numBits.toInt();
    numBits &= 63;
    if (numBits === 0)
        return this;
    else {
        var high = this.high;
        if (numBits < 32) {
            var low = this.low;
            return fromBits((low >>> numBits) | (high << (32 - numBits)), high >>> numBits, this.unsigned);
        } else if (numBits === 32)
            return fromBits(high, 0, this.unsigned);
        else
            return fromBits(high >>> (numBits - 32), 0, this.unsigned);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.sub"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>sub (subtrahend)](#apidoc.element.protobufjs.util.Long.prototype.sub)
- description and source-code
```javascript
function subtract(subtrahend) {
    if (!isLong(subtrahend))
        subtrahend = fromValue(subtrahend);
    return this.add(subtrahend.neg());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.subtract"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>subtract (subtrahend)](#apidoc.element.protobufjs.util.Long.prototype.subtract)
- description and source-code
```javascript
function subtract(subtrahend) {
    if (!isLong(subtrahend))
        subtrahend = fromValue(subtrahend);
    return this.add(subtrahend.neg());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toBytes"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytes (le)](#apidoc.element.protobufjs.util.Long.prototype.toBytes)
- description and source-code
```javascript
toBytes = function (le) {
    return le ? this.toBytesLE() : this.toBytesBE();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toBytesBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytesBE ()](#apidoc.element.protobufjs.util.Long.prototype.toBytesBE)
- description and source-code
```javascript
toBytesBE = function () {
    var hi = this.high,
        lo = this.low;
    return [
        (hi >>> 24) & 0xff,
        (hi >>> 16) & 0xff,
        (hi >>>  8) & 0xff,
         hi         & 0xff,
        (lo >>> 24) & 0xff,
        (lo >>> 16) & 0xff,
        (lo >>>  8) & 0xff,
         lo         & 0xff
    ];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toBytesLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toBytesLE ()](#apidoc.element.protobufjs.util.Long.prototype.toBytesLE)
- description and source-code
```javascript
toBytesLE = function () {
    var hi = this.high,
        lo = this.low;
    return [
         lo         & 0xff,
        (lo >>>  8) & 0xff,
        (lo >>> 16) & 0xff,
        (lo >>> 24) & 0xff,
         hi         & 0xff,
        (hi >>>  8) & 0xff,
        (hi >>> 16) & 0xff,
        (hi >>> 24) & 0xff
    ];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toInt"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toInt ()](#apidoc.element.protobufjs.util.Long.prototype.toInt)
- description and source-code
```javascript
function toInt() {
    return this.unsigned ? this.low >>> 0 : this.low;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toNumber"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toNumber ()](#apidoc.element.protobufjs.util.Long.prototype.toNumber)
- description and source-code
```javascript
function toNumber() {
    if (this.unsigned)
        return ((this.high >>> 0) * TWO_PWR_32_DBL) + (this.low >>> 0);
    return this.high * TWO_PWR_32_DBL + (this.low >>> 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toSigned"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toSigned ()](#apidoc.element.protobufjs.util.Long.prototype.toSigned)
- description and source-code
```javascript
function toSigned() {
    if (!this.unsigned)
        return this;
    return fromBits(this.low, this.high, false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toString"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toString (radix)](#apidoc.element.protobufjs.util.Long.prototype.toString)
- description and source-code
```javascript
function toString(radix) {
    radix = radix || 10;
    if (radix < 2 || 36 < radix)
        throw RangeError('radix');
    if (this.isZero())
        return '0';
    if (this.isNegative()) { // Unsigned Longs are never negative
        if (this.eq(MIN_VALUE)) {
            // We need to change the Long value before it can be negated, so we remove
            // the bottom-most digit in this base and then recurse to do the rest.
            var radixLong = fromNumber(radix),
                div = this.div(radixLong),
                rem1 = div.mul(radixLong).sub(this);
            return div.toString(radix) + rem1.toInt().toString(radix);
        } else
            return '-' + this.neg().toString(radix);
    }

    // Do several (6) digits each time through the loop, so as to
    // minimize the calls to the very expensive emulated div.
    var radixToPower = fromNumber(pow_dbl(radix, 6), this.unsigned),
        rem = this;
    var result = '';
    while (true) {
        var remDiv = rem.div(radixToPower),
            intval = rem.sub(remDiv.mul(radixToPower)).toInt() >>> 0,
            digits = intval.toString(radix);
        rem = remDiv;
        if (rem.isZero())
            return digits + result;
        else {
            while (digits.length < 6)
                digits = '0' + digits;
            result = '' + digits + result;
        }
    }
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.toUnsigned"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>toUnsigned ()](#apidoc.element.protobufjs.util.Long.prototype.toUnsigned)
- description and source-code
```javascript
function toUnsigned() {
    if (this.unsigned)
        return this;
    return fromBits(this.low, this.high, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.Long.prototype.xor"></a>[function <span class="apidocSignatureSpan">protobufjs.util.Long.prototype.</span>xor (other)](#apidoc.element.protobufjs.util.Long.prototype.xor)
- description and source-code
```javascript
function xor(other) {
    if (!isLong(other))
        other = fromValue(other);
    return fromBits(this.low ^ other.low, this.high ^ other.high, this.unsigned);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.LongBits"></a>[module protobufjs.util.LongBits](#apidoc.module.protobufjs.util.LongBits)

#### <a name="apidoc.element.protobufjs.util.LongBits.LongBits"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>LongBits (lo, hi)](#apidoc.element.protobufjs.util.LongBits.LongBits)
- description and source-code
```javascript
function LongBits(lo, hi) {

    // note that the casts below are theoretically unnecessary as of today, but older statically
    // generated converter code might still call the ctor with signed 32bits. kept for compat.

    /**
     * Low bits.
     * @type {number}
     */
    this.lo = lo >>> 0;

    /**
     * High bits.
     * @type {number}
     */
    this.hi = hi >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.from"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>from (value)](#apidoc.element.protobufjs.util.LongBits.from)
- description and source-code
```javascript
function from(value) {
    if (typeof value === "number")
        return LongBits.fromNumber(value);
    if (util.isString(value)) {
        /* istanbul ignore else */
        if (util.Long)
            value = util.Long.fromString(value);
        else
            return LongBits.fromNumber(parseInt(value, 10));
    }
    return value.low || value.high ? new LongBits(value.low >>> 0, value.high >>> 0) : zero;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.fromHash"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>fromHash (hash)](#apidoc.element.protobufjs.util.LongBits.fromHash)
- description and source-code
```javascript
function fromHash(hash) {
    if (hash === zeroHash)
        return zero;
    return new LongBits(
        ( charCodeAt.call(hash, 0)
        | charCodeAt.call(hash, 1) << 8
        | charCodeAt.call(hash, 2) << 16
        | charCodeAt.call(hash, 3) << 24) >>> 0
    ,
        ( charCodeAt.call(hash, 4)
        | charCodeAt.call(hash, 5) << 8
        | charCodeAt.call(hash, 6) << 16
        | charCodeAt.call(hash, 7) << 24) >>> 0
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.fromNumber"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.</span>fromNumber (value)](#apidoc.element.protobufjs.util.LongBits.fromNumber)
- description and source-code
```javascript
function fromNumber(value) {
    if (value === 0)
        return zero;
    var sign = value < 0;
    if (sign)
        value = -value;
    var lo = value >>> 0,
        hi = (value - lo) / 4294967296 >>> 0;
    if (sign) {
        hi = ~hi >>> 0;
        lo = ~lo >>> 0;
        if (++lo > 4294967295) {
            lo = 0;
            if (++hi > 4294967295)
                hi = 0;
        }
    }
    return new LongBits(lo, hi);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.LongBits.prototype"></a>[module protobufjs.util.LongBits.prototype](#apidoc.module.protobufjs.util.LongBits.prototype)

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.length"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>length ()](#apidoc.element.protobufjs.util.LongBits.prototype.length)
- description and source-code
```javascript
function length() {
    var part0 =  this.lo,
        part1 = (this.lo >>> 28 | this.hi << 4) >>> 0,
        part2 =  this.hi >>> 24;
    return part2 === 0
         ? part1 === 0
           ? part0 < 16384
             ? part0 < 128 ? 1 : 2
             : part0 < 2097152 ? 3 : 4
           : part1 < 16384
             ? part1 < 128 ? 5 : 6
             : part1 < 2097152 ? 7 : 8
         : part2 < 128 ? 9 : 10;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.toHash"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toHash ()](#apidoc.element.protobufjs.util.LongBits.prototype.toHash)
- description and source-code
```javascript
function toHash() {
    return String.fromCharCode(
        this.lo        & 255,
        this.lo >>> 8  & 255,
        this.lo >>> 16 & 255,
        this.lo >>> 24      ,
        this.hi        & 255,
        this.hi >>> 8  & 255,
        this.hi >>> 16 & 255,
        this.hi >>> 24
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.toLong"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toLong (unsigned)](#apidoc.element.protobufjs.util.LongBits.prototype.toLong)
- description and source-code
```javascript
function toLong(unsigned) {
    return util.Long
        ? new util.Long(this.lo | 0, this.hi | 0, Boolean(unsigned))
        /* istanbul ignore next */
        : { low: this.lo | 0, high: this.hi | 0, unsigned: Boolean(unsigned) };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.toNumber"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>toNumber (unsigned)](#apidoc.element.protobufjs.util.LongBits.prototype.toNumber)
- description and source-code
```javascript
function toNumber(unsigned) {
    if (!unsigned && this.hi >>> 31) {
        var lo = ~this.lo + 1 >>> 0,
            hi = ~this.hi     >>> 0;
        if (!lo)
            hi = hi + 1 >>> 0;
        return -(lo + hi * 4294967296);
    }
    return this.lo + this.hi * 4294967296;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.zzDecode"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>zzDecode ()](#apidoc.element.protobufjs.util.LongBits.prototype.zzDecode)
- description and source-code
```javascript
function zzDecode() {
    var mask = -(this.lo & 1);
    this.lo  = ((this.lo >>> 1 | this.hi << 31) ^ mask) >>> 0;
    this.hi  = ( this.hi >>> 1                  ^ mask) >>> 0;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.LongBits.prototype.zzEncode"></a>[function <span class="apidocSignatureSpan">protobufjs.util.LongBits.prototype.</span>zzEncode ()](#apidoc.element.protobufjs.util.LongBits.prototype.zzEncode)
- description and source-code
```javascript
function zzEncode() {
    var mask =   this.hi >> 31;
    this.hi  = ((this.hi << 1 | this.lo >>> 31) ^ mask) >>> 0;
    this.lo  = ( this.lo << 1                   ^ mask) >>> 0;
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.ProtocolError"></a>[module protobufjs.util.ProtocolError](#apidoc.module.protobufjs.util.ProtocolError)

#### <a name="apidoc.element.protobufjs.util.ProtocolError.ProtocolError"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>ProtocolError (message, properties)](#apidoc.element.protobufjs.util.ProtocolError.ProtocolError)
- description and source-code
```javascript
function CustomError(message, properties) {

    if (!(this instanceof CustomError))
        return new CustomError(message, properties);

    // Error.call(this, message);
    // ^ just returns a new error instance because the ctor can be called as a function

    Object.defineProperty(this, "message", { get: function() { return message; } });

    /* istanbul ignore next */
    if (Error.captureStackTrace) // node
        Error.captureStackTrace(this, CustomError);
    else
        Object.defineProperty(this, "stack", { value: (new Error()).stack || "" });

    if (properties)
        merge(this, properties);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.ProtocolError.prototype"></a>[module protobufjs.util.ProtocolError.prototype](#apidoc.module.protobufjs.util.ProtocolError.prototype)

#### <a name="apidoc.element.protobufjs.util.ProtocolError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">protobufjs.util.ProtocolError.prototype.</span>constructor (message, properties)](#apidoc.element.protobufjs.util.ProtocolError.prototype.constructor)
- description and source-code
```javascript
function CustomError(message, properties) {

    if (!(this instanceof CustomError))
        return new CustomError(message, properties);

    // Error.call(this, message);
    // ^ just returns a new error instance because the ctor can be called as a function

    Object.defineProperty(this, "message", { get: function() { return message; } });

    /* istanbul ignore next */
    if (Error.captureStackTrace) // node
        Error.captureStackTrace(this, CustomError);
    else
        Object.defineProperty(this, "stack", { value: (new Error()).stack || "" });

    if (properties)
        merge(this, properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.ProtocolError.prototype.toString"></a>[function <span class="apidocSignatureSpan">protobufjs.util.ProtocolError.prototype.</span>toString ()](#apidoc.element.protobufjs.util.ProtocolError.prototype.toString)
- description and source-code
```javascript
function toString() {
    return this.name + ": " + this.message;
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```



# <a name="apidoc.module.protobufjs.util.base64"></a>[module protobufjs.util.base64](#apidoc.module.protobufjs.util.base64)

#### <a name="apidoc.element.protobufjs.util.base64.decode"></a>[function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>decode (string, buffer, offset)](#apidoc.element.protobufjs.util.base64.decode)
- description and source-code
```javascript
function decode(string, buffer, offset) {
    var start = offset;
    var j = 0, // goto index
        t;     // temporary
    for (var i = 0; i < string.length;) {
        var c = string.charCodeAt(i++);
        if (c === 61 && j > 1)
            break;
        if ((c = s64[c]) === undefined)
            throw Error(invalidEncoding);
        switch (j) {
            case 0:
                t = c;
                j = 1;
                break;
            case 1:
                buffer[offset++] = t << 2 | (c & 48) >> 4;
                t = c;
                j = 2;
                break;
            case 2:
                buffer[offset++] = (t & 15) << 4 | (c & 60) >> 2;
                t = c;
                j = 3;
                break;
            case 3:
                buffer[offset++] = (t & 3) << 6 | c;
                j = 0;
                break;
        }
    }
    if (j === 1)
        throw Error(invalidEncoding);
    return offset - start;
}
```
- example usage
```shell
...
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.

'''js
try {
  var decodedMessage = AwesomeMessage.decode(buffer);
} catch (e) {
    if (e instanceof protobuf.util.ProtocolError) {
      // e.instance holds the so far decoded message with missing required fields
    } else {
      // wire format is invalid
    }
}
...
```

#### <a name="apidoc.element.protobufjs.util.base64.encode"></a>[function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>encode (buffer, start, end)](#apidoc.element.protobufjs.util.base64.encode)
- description and source-code
```javascript
function encode(buffer, start, end) {
    var string = []; // alt: new Array(Math.ceil((end - start) / 3) * 4);
    var i = 0, // output index
        j = 0, // goto index
        t;     // temporary
    while (start < end) {
        var b = buffer[start++];
        switch (j) {
            case 0:
                string[i++] = b64[b >> 2];
                t = (b & 3) << 4;
                j = 1;
                break;
            case 1:
                string[i++] = b64[t | b >> 4];
                t = (b & 15) << 2;
                j = 2;
                break;
            case 2:
                string[i++] = b64[t | b >> 6];
                string[i++] = b64[b & 63];
                j = 0;
                break;
        }
    }
    if (j) {
        string[i++] = b64[t];
        string[i  ] = 61;
        if (j === 1)
            string[i + 1] = 61;
    }
    return String.fromCharCode.apply(String, string);
}
```
- example usage
```shell
...
  throw Error(err);
'''

* **Message.encode**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
is an automatically generated message specific encoder expecting a valid message or plain object. Note that this method does not
 implicitly verify the message and that it's up to the user to make sure that the data can actually be encoded properly.

'''js
var buffer = AwesomeMessage.encode(message).finish();
'''

* **Message.encodeDelimited**(message: 'Message|Object' [, writer: 'Writer']): 'Writer'<br />
works like 'Message.encode' but additionally prepends the length of the message as a varint.

* **Message.decode**(reader: 'Reader|Uint8Array'): 'Message'<br />
is an automatically generated message specific decoder. If required fields are missing, it throws a 'util.ProtocolError' with an
 'instance' property set to the so far decoded message. If the wire format is invalid, it throws an 'Error'. The result is a runtime
 message.
...
```

#### <a name="apidoc.element.protobufjs.util.base64.length"></a>[function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>length (string)](#apidoc.element.protobufjs.util.base64.length)
- description and source-code
```javascript
function length(string) {
    var p = string.length;
    if (!p)
        return 0;
    var n = 0;
    while (--p % 4 > 1 && string.charAt(p) === "=")
        ++n;
    return Math.ceil(string.length * 3) / 4 - n;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.base64.test"></a>[function <span class="apidocSignatureSpan">protobufjs.util.base64.</span>test (string)](#apidoc.element.protobufjs.util.base64.test)
- description and source-code
```javascript
function test(string) {
    return /^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==|[A-Za-z0-9+/]{3}=)?$/.test(string);
}
```
- example usage
```shell
...

// Spin up a node process with profiling enabled and process the generated log
if (process.execArgv.indexOf("--prof") < 0) {
process.stdout.write("cleaning up old logs ...\n");
var child_process = require("child_process");
var logRe = /^isolate-[0-9A-F]+-v8\.log$/;
fs.readdirSync(process.cwd()).forEach(function readdirSync_it(file) {
    if (logRe.test(file))
        fs.unlink(file);
});
process.stdout.write("generating profile (may take a while) ...\n");
child_process.execSync("node --prof --trace-deopt " + process.execArgv.join(" ") + " " + process.argv.slice(1).join(" "), {
    cwd: process.cwd(),
    stdio: "inherit"
});
...
```



# <a name="apidoc.module.protobufjs.util.codegen"></a>[module protobufjs.util.codegen](#apidoc.module.protobufjs.util.codegen)

#### <a name="apidoc.element.protobufjs.util.codegen.codegen"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>codegen ()](#apidoc.element.protobufjs.util.codegen.codegen)
- description and source-code
```javascript
function codegen() {
    var params = [],
        src    = [],
        indent = 1,
        inCase = false;
    for (var i = 0; i < arguments.length;)
        params.push(arguments[i++]);

    /**
     * A codegen instance as returned by {@link codegen}, that also is a sprintf-like appender function.
     * @typedef Codegen
     * @type {function}
     * @param {string} format Format string
     * @param {...*} args Replacements
     * @returns {Codegen} Itself
     * @property {function(string=):string} str Stringifies the so far generated function source.
     * @property {function(string=, Object=):function} eof Ends generation and builds the function whilst applying a scope.
     */
    /**/
    function gen() {
        var args = [],
            i = 0;
        for (; i < arguments.length;)
            args.push(arguments[i++]);
        var line = sprintf.apply(null, args);
        var level = indent;
        if (src.length) {
            var prev = src[src.length - 1];

            // block open or one time branch
            if (blockOpenRe.test(prev))
                level = ++indent; // keep
            else if (branchRe.test(prev))
                ++level; // once

            // casing
            if (casingRe.test(prev) && !casingRe.test(line)) {
                level = ++indent;
                inCase = true;
            } else if (inCase && breakRe.test(prev)) {
                level = --indent;
                inCase = false;
            }

            // block close
            if (blockCloseRe.test(line))
                level = --indent;
        }
        for (i = 0; i < level; ++i)
            line = "\t" + line;
        src.push(line);
        return gen;
    }

    /**
     * Stringifies the so far generated function source.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @returns {string} Function source using tabs for indentation
     * @inner
     */
    function str(name) {
        return "function" + (name ? " " + name.replace(/[^\w_$]/g, "_") : "") + "(" + params.join(",") + ") {\n" + src.join("\n") + "\n}";
    }

    gen.str = str;

    /**
     * Ends generation and builds the function whilst applying a scope.
     * @param {string} [name] Function name, defaults to generate an anonymous function
     * @param {Object.<string,*>} [scope] Function scope
     * @returns {function} The generated function, with scope applied if specified
     * @inner
     */
    function eof(name, scope) {
        if (typeof name === "object") {
            scope = name;
            name = undefined;
        }
        var source = gen.str(name);
        if (codegen.verbose)
            console.log("--- codegen ---\n" + source.replace(/^/mg, "> ").replace(/\t/g, "  ")); // eslint-disable-line no-console
        var keys = Object.keys(scope || (scope = {}));
        return Function.apply(null, keys.concat("return " + source)).apply(null, keys.map(function(key) { return scope[key]; })); //
eslint-disable-line no-new-func
        //     ^ Creates a wrapper function with the scoped variable names as its parameters,
        //       calls it with the respective scoped variable values ^
        //       and returns our brand-new properly scoped function.
        //
        // This works because "Invoking the Function constructor as a function (without using the
        // new operator) has the same effect as invoking it as a constructor."
        // https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Function
    }

    gen.eof = eof;

    return gen;
}
```
- example usage
```shell
...
/**
 * Generates a decoder specific to the specified message type.
 * @param {Type} mtype Message type
 * @returns {Codegen} Codegen instance
 */
function decoder(mtype) {
/* eslint-disable no-unexpected-multiline */
var gen = util.codegen("r", "l")
("if(!(r instanceof Reader))")
    ("r=Reader.create(r)")
("var c=l===undefined?r.len:r.pos+l,m=new this.ctor" + (mtype.fieldsArray.filter(function(field) { return field.map; }).length ? ",
k" : ""))
("while(r.pos<c){")
    ("var t=r.uint32()");
if (mtype.group) gen
    ("if((t&7)===4)")
...
```

#### <a name="apidoc.element.protobufjs.util.codegen.sprintf"></a>[function <span class="apidocSignatureSpan">protobufjs.util.codegen.</span>sprintf (format)](#apidoc.element.protobufjs.util.codegen.sprintf)
- description and source-code
```javascript
function sprintf(format) {
    var args = [],
        i = 1;
    for (; i < arguments.length;)
        args.push(arguments[i++]);
    i = 0;
    format = format.replace(/%([dfjs])/g, function($0, $1) {
        switch ($1) {
            case "d":
                return Math.floor(args[i++]);
            case "f":
                return Number(args[i++]);
            case "j":
                return JSON.stringify(args[i++]);
            default:
                return args[i++];
        }
    });
    if (i !== args.length)
        throw Error("argument count mismatch");
    return format;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.fetch"></a>[module protobufjs.util.fetch](#apidoc.module.protobufjs.util.fetch)

#### <a name="apidoc.element.protobufjs.util.fetch.fetch"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>fetch (filename, options, callback)](#apidoc.element.protobufjs.util.fetch.fetch)
- description and source-code
```javascript
function fetch(filename, options, callback) {
    if (typeof options === "function") {
        callback = options;
        options = {};
    } else if (!options)
        options = {};

    if (!callback)
        return asPromise(fetch, this, filename, options); // eslint-disable-line no-invalid-this

    // if a node-like filesystem is present, try it first but fall back to XHR if nothing is found.
    if (!options.xhr && fs && fs.readFile)
        return fs.readFile(filename, function fetchReadFileCallback(err, contents) {
            return err && typeof XMLHttpRequest !== "undefined"
                ? fetch.xhr(filename, options, callback)
                : err
                ? callback(err)
                : callback(null, options.binary ? contents : contents.toString("utf8"));
        });

    // use the XHR version otherwise.
    return fetch.xhr(filename, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.fetch.xhr"></a>[function <span class="apidocSignatureSpan">protobufjs.util.fetch.</span>xhr (filename, options, callback)](#apidoc.element.protobufjs.util.fetch.xhr)
- description and source-code
```javascript
function fetch_xhr(filename, options, callback) {
    var xhr = new XMLHttpRequest();
    xhr.onreadystatechange /* works everywhere */ = function fetchOnReadyStateChange() {

        if (xhr.readyState !== 4)
            return undefined;

        // local cors security errors return status 0 / empty string, too. afaik this cannot be
        // reliably distinguished from an actually empty file for security reasons. feel free
        // to send a pull request if you are aware of a solution.
        if (xhr.status !== 0 && xhr.status !== 200)
            return callback(Error("status " + xhr.status));

        // if binary data is expected, make sure that some sort of array is returned, even if
        // ArrayBuffers are not supported. the binary string fallback, however, is unsafe.
        if (options.binary) {
            var buffer = xhr.response;
            if (!buffer) {
                buffer = [];
                for (var i = 0; i < xhr.responseText.length; ++i)
                    buffer.push(xhr.responseText.charCodeAt(i) & 255);
            }
            return callback(null, typeof Uint8Array !== "undefined" ? new Uint8Array(buffer) : buffer);
        }
        return callback(null, xhr.responseText);
    };

    if (options.binary) {
        // ref: https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Sending_and_Receiving_Binary_Data#Receiving_binary_data_in_older_browsers
        if ("overrideMimeType" in xhr)
            xhr.overrideMimeType("text/plain; charset=x-user-defined");
        xhr.responseType = "arraybuffer";
    }

    xhr.open("GET", filename);
    xhr.send();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.float"></a>[module protobufjs.util.float](#apidoc.module.protobufjs.util.float)

#### <a name="apidoc.element.protobufjs.util.float.float"></a>[function <span class="apidocSignatureSpan">protobufjs.util.</span>float (exports)](#apidoc.element.protobufjs.util.float.float)
- description and source-code
```javascript
function factory(exports) {

    // float: typed array
    if (typeof Float32Array !== "undefined") (function() {

        var f32 = new Float32Array([ -0 ]),
            f8b = new Uint8Array(f32.buffer),
            le  = f8b[3] === 128;

        function writeFloat_f32_cpy(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
        }

        function writeFloat_f32_rev(val, buf, pos) {
            f32[0] = val;
            buf[pos    ] = f8b[3];
            buf[pos + 1] = f8b[2];
            buf[pos + 2] = f8b[1];
            buf[pos + 3] = f8b[0];
        }

        /* istanbul ignore next */
        exports.writeFloatLE = le ? writeFloat_f32_cpy : writeFloat_f32_rev;
        /* istanbul ignore next */
        exports.writeFloatBE = le ? writeFloat_f32_rev : writeFloat_f32_cpy;

        function readFloat_f32_cpy(buf, pos) {
            f8b[0] = buf[pos    ];
            f8b[1] = buf[pos + 1];
            f8b[2] = buf[pos + 2];
            f8b[3] = buf[pos + 3];
            return f32[0];
        }

        function readFloat_f32_rev(buf, pos) {
            f8b[3] = buf[pos    ];
            f8b[2] = buf[pos + 1];
            f8b[1] = buf[pos + 2];
            f8b[0] = buf[pos + 3];
            return f32[0];
        }

        /* istanbul ignore next */
        exports.readFloatLE = le ? readFloat_f32_cpy : readFloat_f32_rev;
        /* istanbul ignore next */
        exports.readFloatBE = le ? readFloat_f32_rev : readFloat_f32_cpy;

    // float: ieee754
    })(); else (function() {

        function writeFloat_ieee754(writeUint, val, buf, pos) {
            var sign = val < 0 ? 1 : 0;
            if (sign)
                val = -val;
            if (val === 0)
                writeUint(1 / val > 0 ? /* positive */ 0 : /* negative 0 */ 2147483648, buf, pos);
            else if (isNaN(val))
                writeUint(2143289344, buf, pos);
            else if (val > 3.4028234663852886e+38) // +-Infinity
                writeUint((sign << 31 | 2139095040) >>> 0, buf, pos);
            else if (val < 1.1754943508222875e-38) // denormal
                writeUint((sign << 31 | Math.round(val / 1.401298464324817e-45)) >>> 0, buf, pos);
            else {
                var exponent = Math.floor(Math.log(val) / Math.LN2),
                    mantissa = Math.round(val * Math.pow(2, -exponent) * 8388608) & 8388607;
                writeUint((sign << 31 | exponent + 127 << 23 | mantissa) >>> 0, buf, pos);
            }
        }

        exports.writeFloatLE = writeFloat_ieee754.bind(null, writeUintLE);
        exports.writeFloatBE = writeFloat_ieee754.bind(null, writeUintBE);

        function readFloat_ieee754(readUint, buf, pos) {
            var uint = readUint(buf, pos),
                sign = (uint >> 31) * 2 + 1,
                exponent = uint >>> 23 & 255,
                mantissa = uint & 8388607;
            return exponent === 255
                ? mantissa
                ? NaN
                : sign * Infinity
                : exponent === 0 // denormal
                ? sign * 1.401298464324817e-45 * mantissa
                : sign * Math.pow(2, exponent - 150) * (mantissa + 8388608);
        }

        exports.readFloatLE = readFloat_ieee754.bind(null, readUintLE);
        exports.readFloatBE = readFloat_ieee754.bind(null, readUintBE);

    })();

    // double: typed array
    if (typeof Float64Array !== "undefined") (function() {

        var f64 = new Float64Array([-0]),
            f8b = new Uint8Array(f64.buffer),
            le  = f8b[7] === 128;

        function writeDouble_f64_cpy(val, buf, pos) {
            f64[0] = val;
            buf[pos    ] = f8b[0];
            buf[pos + 1] = f8b[1];
            buf[pos + 2] = f8b[2];
            buf[pos + 3] = f8b[3];
            buf[pos + 4] = f8b[4];
            buf[pos + 5] = f8b[5];
            buf[pos + 6] = f8b[6] ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.readDoubleBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readDoubleBE (buf, pos)](#apidoc.element.protobufjs.util.float.readDoubleBE)
- description and source-code
```javascript
function readDouble_f64_rev(buf, pos) {
    f8b[7] = buf[pos    ];
    f8b[6] = buf[pos + 1];
    f8b[5] = buf[pos + 2];
    f8b[4] = buf[pos + 3];
    f8b[3] = buf[pos + 4];
    f8b[2] = buf[pos + 5];
    f8b[1] = buf[pos + 6];
    f8b[0] = buf[pos + 7];
    return f64[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.readDoubleLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readDoubleLE (buf, pos)](#apidoc.element.protobufjs.util.float.readDoubleLE)
- description and source-code
```javascript
function readDouble_f64_cpy(buf, pos) {
    f8b[0] = buf[pos    ];
    f8b[1] = buf[pos + 1];
    f8b[2] = buf[pos + 2];
    f8b[3] = buf[pos + 3];
    f8b[4] = buf[pos + 4];
    f8b[5] = buf[pos + 5];
    f8b[6] = buf[pos + 6];
    f8b[7] = buf[pos + 7];
    return f64[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.readFloatBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readFloatBE (buf, pos)](#apidoc.element.protobufjs.util.float.readFloatBE)
- description and source-code
```javascript
function readFloat_f32_rev(buf, pos) {
    f8b[3] = buf[pos    ];
    f8b[2] = buf[pos + 1];
    f8b[1] = buf[pos + 2];
    f8b[0] = buf[pos + 3];
    return f32[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.readFloatLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>readFloatLE (buf, pos)](#apidoc.element.protobufjs.util.float.readFloatLE)
- description and source-code
```javascript
function readFloat_f32_cpy(buf, pos) {
    f8b[0] = buf[pos    ];
    f8b[1] = buf[pos + 1];
    f8b[2] = buf[pos + 2];
    f8b[3] = buf[pos + 3];
    return f32[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.writeDoubleBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeDoubleBE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeDoubleBE)
- description and source-code
```javascript
function writeDouble_f64_rev(val, buf, pos) {
    f64[0] = val;
    buf[pos    ] = f8b[7];
    buf[pos + 1] = f8b[6];
    buf[pos + 2] = f8b[5];
    buf[pos + 3] = f8b[4];
    buf[pos + 4] = f8b[3];
    buf[pos + 5] = f8b[2];
    buf[pos + 6] = f8b[1];
    buf[pos + 7] = f8b[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.writeDoubleLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeDoubleLE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeDoubleLE)
- description and source-code
```javascript
function writeDouble_f64_cpy(val, buf, pos) {
    f64[0] = val;
    buf[pos    ] = f8b[0];
    buf[pos + 1] = f8b[1];
    buf[pos + 2] = f8b[2];
    buf[pos + 3] = f8b[3];
    buf[pos + 4] = f8b[4];
    buf[pos + 5] = f8b[5];
    buf[pos + 6] = f8b[6];
    buf[pos + 7] = f8b[7];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.writeFloatBE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeFloatBE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeFloatBE)
- description and source-code
```javascript
function writeFloat_f32_rev(val, buf, pos) {
    f32[0] = val;
    buf[pos    ] = f8b[3];
    buf[pos + 1] = f8b[2];
    buf[pos + 2] = f8b[1];
    buf[pos + 3] = f8b[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.float.writeFloatLE"></a>[function <span class="apidocSignatureSpan">protobufjs.util.float.</span>writeFloatLE (val, buf, pos)](#apidoc.element.protobufjs.util.float.writeFloatLE)
- description and source-code
```javascript
function writeFloat_f32_cpy(val, buf, pos) {
    f32[0] = val;
    buf[pos    ] = f8b[0];
    buf[pos + 1] = f8b[1];
    buf[pos + 2] = f8b[2];
    buf[pos + 3] = f8b[3];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.path"></a>[module protobufjs.util.path](#apidoc.module.protobufjs.util.path)

#### <a name="apidoc.element.protobufjs.util.path.isAbsolute"></a>[function <span class="apidocSignatureSpan">protobufjs.util.path.</span>isAbsolute (path)](#apidoc.element.protobufjs.util.path.isAbsolute)
- description and source-code
```javascript
function isAbsolute(path) {
    return /^(?:\/|\w+:)/.test(path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.path.normalize"></a>[function <span class="apidocSignatureSpan">protobufjs.util.path.</span>normalize (path)](#apidoc.element.protobufjs.util.path.normalize)
- description and source-code
```javascript
function normalize(path) {
    path = path.replace(/\\/g, "/")
               .replace(/\/{2,}/g, "/");
    var parts    = path.split("/"),
        absolute = isAbsolute(path),
        prefix   = "";
    if (absolute)
        prefix = parts.shift() + "/";
    for (var i = 0; i < parts.length;) {
        if (parts[i] === "..") {
            if (i > 0 && parts[i - 1] !== "..")
                parts.splice(--i, 2);
            else if (absolute)
                parts.splice(i, 1);
            else
                ++i;
        } else if (parts[i] === ".")
            parts.splice(i, 1);
        else
            ++i;
    }
    return prefix + parts.join("/");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.path.resolve"></a>[function <span class="apidocSignatureSpan">protobufjs.util.path.</span>resolve (originPath, includePath, alreadyNormalized)](#apidoc.element.protobufjs.util.path.resolve)
- description and source-code
```javascript
function resolve(originPath, includePath, alreadyNormalized) {
    if (!alreadyNormalized)
        includePath = normalize(includePath);
    if (isAbsolute(includePath))
        return includePath;
    if (!alreadyNormalized)
        originPath = normalize(originPath);
    return (originPath = originPath.replace(/(?:\/|^)[^/]+$/, "")).length ? normalize(originPath + "/" + includePath) : includePath
;
}
```
- example usage
```shell
...
        protobuf.Root.fromJSON(json).resolveAll();
return;
}

var Test, data, count;

if (process.argv.indexOf("--alt") < 0) {
root = protobuf.parse(fs.readFileSync(require.resolve("../bench/bench.proto")).toString("utf8")).root;
Test = root.lookup("Test");
json = JSON.stringify(root);
data = require("../bench/bench.json");
count = 10000000;
process.stdout.write("bench.proto");
} else {
root = protobuf.parse(fs.readFileSync(require.resolve("../tests/data/mapbox/vector_tile.proto")).toString("utf8")).root;
...
```



# <a name="apidoc.module.protobufjs.util.toJSONOptions"></a>[module protobufjs.util.toJSONOptions](#apidoc.module.protobufjs.util.toJSONOptions)

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.bytes"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>bytes ()](#apidoc.element.protobufjs.util.toJSONOptions.bytes)
- description and source-code
```javascript
function String() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.enums"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>enums ()](#apidoc.element.protobufjs.util.toJSONOptions.enums)
- description and source-code
```javascript
function String() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.longs"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.</span>longs ()](#apidoc.element.protobufjs.util.toJSONOptions.longs)
- description and source-code
```javascript
function String() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.toJSONOptions.longs.prototype"></a>[module protobufjs.util.toJSONOptions.longs.prototype](#apidoc.module.protobufjs.util.toJSONOptions.longs.prototype)

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.entityify"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>entityify ()](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.entityify)
- description and source-code
```javascript
entityify = function (){return this.replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;"
)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isAlpha"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>isAlpha ( )](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isAlpha)
- description and source-code
```javascript
isAlpha = function ( ){return this>="a"&&this<="z\uffff"||this>="A"&&this<="Z\uffff"}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isDigit"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>isDigit ()](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.isDigit)
- description and source-code
```javascript
isDigit = function (){return this>="0"&&
this<="9"}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.supplant"></a>[function <span class="apidocSignatureSpan">protobufjs.util.toJSONOptions.longs.prototype.</span>supplant (e)](#apidoc.element.protobufjs.util.toJSONOptions.longs.prototype.supplant)
- description and source-code
```javascript
supplant = function (e){return this.replace(/\{([^{}]*)\}/g,function(t,n){var r=e[n];return typeof
r=="string"||typeof r=="number"?r:t})}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.protobufjs.util.utf8"></a>[module protobufjs.util.utf8](#apidoc.module.protobufjs.util.utf8)

#### <a name="apidoc.element.protobufjs.util.utf8.length"></a>[function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>length (string)](#apidoc.element.protobufjs.util.utf8.length)
- description and source-code
```javascript
function utf8_length(string) {
    var len = 0,
        c = 0;
    for (var i = 0; i < string.length; ++i) {
        c = string.charCodeAt(i);
        if (c < 128)
            len += 1;
        else if (c < 2048)
            len += 2;
        else if ((c & 0xFC00) === 0xD800 && (string.charCodeAt(i + 1) & 0xFC00) === 0xDC00) {
            ++i;
            len += 4;
        } else
            len += 3;
    }
    return len;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.utf8.read"></a>[function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>read (buffer, start, end)](#apidoc.element.protobufjs.util.utf8.read)
- description and source-code
```javascript
function utf8_read(buffer, start, end) {
    var len = end - start;
    if (len < 1)
        return "";
    var parts = null,
        chunk = [],
        i = 0, // char offset
        t;     // temporary
    while (start < end) {
        t = buffer[start++];
        if (t < 128)
            chunk[i++] = t;
        else if (t > 191 && t < 224)
            chunk[i++] = (t & 31) << 6 | buffer[start++] & 63;
        else if (t > 239 && t < 365) {
            t = ((t & 7) << 18 | (buffer[start++] & 63) << 12 | (buffer[start++] & 63) << 6 | buffer[start++] & 63) - 0x10000;
            chunk[i++] = 0xD800 + (t >> 10);
            chunk[i++] = 0xDC00 + (t & 1023);
        } else
            chunk[i++] = (t & 15) << 12 | (buffer[start++] & 63) << 6 | buffer[start++] & 63;
        if (i > 8191) {
            (parts || (parts = [])).push(String.fromCharCode.apply(String, chunk));
            i = 0;
        }
    }
    if (parts) {
        if (i)
            parts.push(String.fromCharCode.apply(String, chunk.slice(0, i)));
        return parts.join("");
    }
    return String.fromCharCode.apply(String, chunk.slice(0, i));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.protobufjs.util.utf8.write"></a>[function <span class="apidocSignatureSpan">protobufjs.util.utf8.</span>write (string, buffer, offset)](#apidoc.element.protobufjs.util.utf8.write)
- description and source-code
```javascript
function utf8_write(string, buffer, offset) {
    var start = offset,
        c1, // character 1
        c2; // character 2
    for (var i = 0; i < string.length; ++i) {
        c1 = string.charCodeAt(i);
        if (c1 < 128) {
            buffer[offset++] = c1;
        } else if (c1 < 2048) {
            buffer[offset++] = c1 >> 6       | 192;
            buffer[offset++] = c1       & 63 | 128;
        } else if ((c1 & 0xFC00) === 0xD800 && ((c2 = string.charCodeAt(i + 1)) & 0xFC00) === 0xDC00) {
            c1 = 0x10000 + ((c1 & 0x03FF) << 10) + (c2 & 0x03FF);
            ++i;
            buffer[offset++] = c1 >> 18      | 240;
            buffer[offset++] = c1 >> 12 & 63 | 128;
            buffer[offset++] = c1 >> 6  & 63 | 128;
            buffer[offset++] = c1       & 63 | 128;
        } else {
            buffer[offset++] = c1 >> 12      | 224;
            buffer[offset++] = c1 >> 6  & 63 | 128;
            buffer[offset++] = c1       & 63 | 128;
        }
    }
    return offset - start;
}
```
- example usage
```shell
...
var fs   = require("fs"),
path = require("path");

// A profiling stub to measure encoding / decoding performance using benchmark data.

var commands = ["encode", "decode", "encode-browser", "decode-browser", "fromjson"];
if (commands.indexOf(process.argv[2]) < 0) { // 0: node, 1: prof.js
process.stderr.write("usage: " + path.basename(process.argv[1]) + " <" + commands.join("|") + "> [iterations=10000000]\n");
return;
}

// Spin up a node process with profiling enabled and process the generated log
if (process.execArgv.indexOf("--prof") < 0) {
process.stdout.write("cleaning up old logs ...\n");
var child_process = require("child_process");
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
