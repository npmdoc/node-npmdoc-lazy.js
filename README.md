# api documentation for  [lazy.js (v0.5.0)](http://dtao.github.io/lazy.js/)  [![npm package](https://img.shields.io/npm/v/npmdoc-lazy.js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-lazy.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-lazy.js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-lazy.js)
#### Like Underscore, but lazier

[![NPM](https://nodei.co/npm/lazy.js.png?downloads=true)](https://www.npmjs.com/package/lazy.js)

[![apidoc](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-lazy.js_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-lazy.js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-lazy.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Tao",
        "email": "daniel.tao@gmail.com",
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
            "name": "dtao",
            "email": "daniel.tao@gmail.com"
        }
    ],
    "name": "lazy.js",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module lazy.js](#apidoc.module.lazy.js)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>ArrayLikeSequence ()](#apidoc.element.lazy.js.ArrayLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>AsyncHandle (cancelFn)](#apidoc.element.lazy.js.AsyncHandle)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>AsyncSequence (parent, interval)](#apidoc.element.lazy.js.AsyncSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.GeneratedSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>ObjectLikeSequence ()](#apidoc.element.lazy.js.ObjectLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>Sequence ()](#apidoc.element.lazy.js.Sequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>StreamLikeSequence ()](#apidoc.element.lazy.js.StreamLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>StringLikeSequence ()](#apidoc.element.lazy.js.StringLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>clone (target)](#apidoc.element.lazy.js.clone)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>createWrapper (initializer)](#apidoc.element.lazy.js.createWrapper)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>deprecate (message, fn)](#apidoc.element.lazy.js.deprecate)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>generate (generatorFn, length)](#apidoc.element.lazy.js.generate)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>identity (x)](#apidoc.element.lazy.js.identity)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>isES6Generator (fn)](#apidoc.element.lazy.js.isES6Generator)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.ArrayLikeSequence ()](#apidoc.element.lazy.js.js.ArrayLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncHandle (cancelFn)](#apidoc.element.lazy.js.js.AsyncHandle)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncSequence (parent, interval)](#apidoc.element.lazy.js.js.AsyncSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.js.GeneratedSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.ObjectLikeSequence ()](#apidoc.element.lazy.js.js.ObjectLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.Sequence ()](#apidoc.element.lazy.js.js.Sequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.StreamLikeSequence ()](#apidoc.element.lazy.js.js.StreamLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>js.StringLikeSequence ()](#apidoc.element.lazy.js.js.StringLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>makeHttpRequest (url)](#apidoc.element.lazy.js.makeHttpRequest)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>noop ()](#apidoc.element.lazy.js.noop)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>parseJSON (json)](#apidoc.element.lazy.js.parseJSON)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>range ()](#apidoc.element.lazy.js.range)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>readFile (path, encoding)](#apidoc.element.lazy.js.readFile)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>repeat (value, count)](#apidoc.element.lazy.js.repeat)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>strict ()](#apidoc.element.lazy.js.strict)
1.  object <span class="apidocSignatureSpan">lazy.js.</span>extensions
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.ArrayLikeSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncHandle.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.GeneratedSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.ObjectLikeSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.Sequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.StreamLikeSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.StringLikeSequence.prototype
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.extensions
1.  object <span class="apidocSignatureSpan">lazy.js.</span>js.util
1.  string <span class="apidocSignatureSpan">lazy.js.</span>VERSION

#### [module lazy.js.ArrayLikeSequence](#apidoc.module.lazy.js.ArrayLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>ArrayLikeSequence ()](#apidoc.element.lazy.js.ArrayLikeSequence.ArrayLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.ArrayLikeSequence.define)

#### [module lazy.js.ArrayLikeSequence.prototype](#apidoc.module.lazy.js.ArrayLikeSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>concat (var_args)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.concat)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.each)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.filter)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>first (count)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.first)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>get (i)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.get)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>getIndex ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIndex)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIterator)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>length ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.length)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>map (mapFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.map)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>pop ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.pop)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>push (value)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.push)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>rest (count)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.rest)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>shift ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.shift)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>slice (begin, end)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.slice)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>uniq (keyFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.uniq)
1.  [function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>unshift (value)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.unshift)

#### [module lazy.js.AsyncHandle](#apidoc.module.lazy.js.AsyncHandle)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>AsyncHandle (cancelFn)](#apidoc.element.lazy.js.AsyncHandle.AsyncHandle)

#### [module lazy.js.AsyncHandle.prototype](#apidoc.module.lazy.js.AsyncHandle.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>_reject (reason)](#apidoc.element.lazy.js.AsyncHandle.prototype._reject)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>_resolve (value)](#apidoc.element.lazy.js.AsyncHandle.prototype._resolve)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>cancel ()](#apidoc.element.lazy.js.AsyncHandle.prototype.cancel)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>onComplete (callback)](#apidoc.element.lazy.js.AsyncHandle.prototype.onComplete)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>onError (callback)](#apidoc.element.lazy.js.AsyncHandle.prototype.onError)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>then (onFulfilled, onRejected)](#apidoc.element.lazy.js.AsyncHandle.prototype.then)

#### [module lazy.js.AsyncSequence](#apidoc.module.lazy.js.AsyncSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>AsyncSequence (parent, interval)](#apidoc.element.lazy.js.AsyncSequence.AsyncSequence)

#### [module lazy.js.AsyncSequence.prototype](#apidoc.module.lazy.js.AsyncSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>async ()](#apidoc.element.lazy.js.AsyncSequence.prototype.async)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>contains (value)](#apidoc.element.lazy.js.AsyncSequence.prototype.contains)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.AsyncSequence.prototype.each)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>find (predicate)](#apidoc.element.lazy.js.AsyncSequence.prototype.find)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.AsyncSequence.prototype.getIterator)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>indexOf (value)](#apidoc.element.lazy.js.AsyncSequence.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.AsyncSequence.prototype.isAsync)
1.  [function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.AsyncSequence.prototype.reverse)

#### [module lazy.js.GeneratedSequence](#apidoc.module.lazy.js.GeneratedSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.GeneratedSequence.GeneratedSequence)

#### [module lazy.js.GeneratedSequence.prototype](#apidoc.module.lazy.js.GeneratedSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.GeneratedSequence.prototype.each)
1.  [function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.getIterator)
1.  [function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.isAsync)
1.  [function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>length ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.length)

#### [module lazy.js.ObjectLikeSequence](#apidoc.module.lazy.js.ObjectLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>ObjectLikeSequence ()](#apidoc.element.lazy.js.ObjectLikeSequence.ObjectLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.ObjectLikeSequence.define)

#### [module lazy.js.ObjectLikeSequence.prototype](#apidoc.module.lazy.js.ObjectLikeSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>assign (other)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.assign)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>async ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.async)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>defaults (defaults)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.defaults)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>extend (other)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.extend)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.filter)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>functions ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.functions)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>get (key)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.get)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>invert ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.invert)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>keys ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.keys)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>merge (var_args)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.merge)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>methods ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.methods)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>omit (properties)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.omit)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>pairs ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.pairs)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>pick (properties)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.pick)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>toArray ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.toArray)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>toObject ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.toObject)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>value ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.value)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>values ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.values)
1.  [function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>watch (propertyNames)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.watch)

#### [module lazy.js.Sequence](#apidoc.module.lazy.js.Sequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>Sequence ()](#apidoc.element.lazy.js.Sequence.Sequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.Sequence.define)

#### [module lazy.js.Sequence.prototype](#apidoc.module.lazy.js.Sequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>all (predicate)](#apidoc.element.lazy.js.Sequence.prototype.all)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>any (predicate)](#apidoc.element.lazy.js.Sequence.prototype.any)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>apply (source)](#apidoc.element.lazy.js.Sequence.prototype.apply)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>async (interval)](#apidoc.element.lazy.js.Sequence.prototype.async)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>chunk (size)](#apidoc.element.lazy.js.Sequence.prototype.chunk)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>collect (mapFn)](#apidoc.element.lazy.js.Sequence.prototype.collect)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>compact ()](#apidoc.element.lazy.js.Sequence.prototype.compact)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>concat (var_args)](#apidoc.element.lazy.js.Sequence.prototype.concat)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>consecutive (count)](#apidoc.element.lazy.js.Sequence.prototype.consecutive)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>contains (value)](#apidoc.element.lazy.js.Sequence.prototype.contains)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>countBy (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.countBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>detect (predicate)](#apidoc.element.lazy.js.Sequence.prototype.detect)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>difference (var_args)](#apidoc.element.lazy.js.Sequence.prototype.difference)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>drop (count)](#apidoc.element.lazy.js.Sequence.prototype.drop)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>dropWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.dropWhile)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.Sequence.prototype.each)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>every (predicate)](#apidoc.element.lazy.js.Sequence.prototype.every)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.Sequence.prototype.filter)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>find (predicate)](#apidoc.element.lazy.js.Sequence.prototype.find)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>findWhere (properties)](#apidoc.element.lazy.js.Sequence.prototype.findWhere)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>first (count)](#apidoc.element.lazy.js.Sequence.prototype.first)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>flatten ()](#apidoc.element.lazy.js.Sequence.prototype.flatten)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>foldl (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.foldl)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>foldr (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.foldr)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>forEach (fn)](#apidoc.element.lazy.js.Sequence.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>get (i)](#apidoc.element.lazy.js.Sequence.prototype.get)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>getIndex ()](#apidoc.element.lazy.js.Sequence.prototype.getIndex)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.Sequence.prototype.getIterator)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>groupBy (keyFn, valFn)](#apidoc.element.lazy.js.Sequence.prototype.groupBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>head (count)](#apidoc.element.lazy.js.Sequence.prototype.head)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>indexBy (keyFn, valFn)](#apidoc.element.lazy.js.Sequence.prototype.indexBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>indexOf (value)](#apidoc.element.lazy.js.Sequence.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>initial (count)](#apidoc.element.lazy.js.Sequence.prototype.initial)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>inject (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.inject)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>intersection (var_args)](#apidoc.element.lazy.js.Sequence.prototype.intersection)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>invoke (methodName)](#apidoc.element.lazy.js.Sequence.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.Sequence.prototype.isAsync)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>isEmpty ()](#apidoc.element.lazy.js.Sequence.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>join (delimiter)](#apidoc.element.lazy.js.Sequence.prototype.join)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>last (count)](#apidoc.element.lazy.js.Sequence.prototype.last)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>lastIndexOf (value)](#apidoc.element.lazy.js.Sequence.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>map (mapFn)](#apidoc.element.lazy.js.Sequence.prototype.map)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>max (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.max)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>maxBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.maxBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>memoize ()](#apidoc.element.lazy.js.Sequence.prototype.memoize)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>min (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.min)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>minBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.minBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>none (predicate)](#apidoc.element.lazy.js.Sequence.prototype.none)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>ofType (type)](#apidoc.element.lazy.js.Sequence.prototype.ofType)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>pipe (destination)](#apidoc.element.lazy.js.Sequence.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>pluck (property)](#apidoc.element.lazy.js.Sequence.prototype.pluck)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reduce (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.reduce)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reduceRight (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.reduceRight)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reject (rejectFn)](#apidoc.element.lazy.js.Sequence.prototype.reject)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>rest (count)](#apidoc.element.lazy.js.Sequence.prototype.rest)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.Sequence.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>root ()](#apidoc.element.lazy.js.Sequence.prototype.root)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>select (filterFn)](#apidoc.element.lazy.js.Sequence.prototype.select)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>shuffle ()](#apidoc.element.lazy.js.Sequence.prototype.shuffle)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>size ()](#apidoc.element.lazy.js.Sequence.prototype.size)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>skip (count)](#apidoc.element.lazy.js.Sequence.prototype.skip)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>skipWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.skipWhile)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>some (predicate)](#apidoc.element.lazy.js.Sequence.prototype.some)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sort (sortFn, descending)](#apidoc.element.lazy.js.Sequence.prototype.sort)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sortBy (sortFn, descending)](#apidoc.element.lazy.js.Sequence.prototype.sortBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sortedIndex (value)](#apidoc.element.lazy.js.Sequence.prototype.sortedIndex)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sum (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.sum)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sumBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.sumBy)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>tail (count)](#apidoc.element.lazy.js.Sequence.prototype.tail)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>take (count)](#apidoc.element.lazy.js.Sequence.prototype.take)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>takeWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.takeWhile)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>tap (callback)](#apidoc.element.lazy.js.Sequence.prototype.tap)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toArray ()](#apidoc.element.lazy.js.Sequence.prototype.toArray)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toObject ()](#apidoc.element.lazy.js.Sequence.prototype.toObject)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toStream (options)](#apidoc.element.lazy.js.Sequence.prototype.toStream)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toString (delimiter)](#apidoc.element.lazy.js.Sequence.prototype.toString)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>union (var_args)](#apidoc.element.lazy.js.Sequence.prototype.union)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>uniq (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.uniq)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>unique (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.unique)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>value ()](#apidoc.element.lazy.js.Sequence.prototype.value)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>where (properties)](#apidoc.element.lazy.js.Sequence.prototype.where)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>without (var_args)](#apidoc.element.lazy.js.Sequence.prototype.without)
1.  [function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>zip (var_args)](#apidoc.element.lazy.js.Sequence.prototype.zip)

#### [module lazy.js.StreamLikeSequence](#apidoc.module.lazy.js.StreamLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>StreamLikeSequence ()](#apidoc.element.lazy.js.StreamLikeSequence.StreamLikeSequence)

#### [module lazy.js.StreamLikeSequence.prototype](#apidoc.module.lazy.js.StreamLikeSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>cancelCallback (immediate)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.cancelCallback)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.StreamLikeSequence.prototype.isAsync)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>lines ()](#apidoc.element.lazy.js.StreamLikeSequence.prototype.lines)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>match (pattern)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.match)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>onNextCallback (callback, arg1, arg2, arg3)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.onNextCallback)
1.  [function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>split (delimiter)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.split)

#### [module lazy.js.StringLikeSequence](#apidoc.module.lazy.js.StringLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.</span>StringLikeSequence ()](#apidoc.element.lazy.js.StringLikeSequence.StringLikeSequence)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.StringLikeSequence.define)

#### [module lazy.js.StringLikeSequence.prototype](#apidoc.module.lazy.js.StringLikeSequence.prototype)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>charAt (i)](#apidoc.element.lazy.js.StringLikeSequence.prototype.charAt)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>charCodeAt (i)](#apidoc.element.lazy.js.StringLikeSequence.prototype.charCodeAt)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>contains (substring)](#apidoc.element.lazy.js.StringLikeSequence.prototype.contains)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>drop (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.drop)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>endsWith (suffix)](#apidoc.element.lazy.js.StringLikeSequence.prototype.endsWith)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>first (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.first)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.getIterator)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>indexOf (substring, startIndex)](#apidoc.element.lazy.js.StringLikeSequence.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>last (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.last)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>lastIndexOf (substring, startIndex)](#apidoc.element.lazy.js.StringLikeSequence.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>mapString (mapFn)](#apidoc.element.lazy.js.StringLikeSequence.prototype.mapString)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>match (pattern)](#apidoc.element.lazy.js.StringLikeSequence.prototype.match)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>split (delimiter)](#apidoc.element.lazy.js.StringLikeSequence.prototype.split)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>startsWith (prefix)](#apidoc.element.lazy.js.StringLikeSequence.prototype.startsWith)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>substring (start, stop)](#apidoc.element.lazy.js.StringLikeSequence.prototype.substring)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toLowerCase ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toLowerCase)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toString ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toString)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toUpperCase ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toUpperCase)
1.  [function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>value ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.value)

#### [module lazy.js.extensions](#apidoc.module.lazy.js.extensions)
1.  [function <span class="apidocSignatureSpan">lazy.js.extensions.</span>0 (source)](#apidoc.element.lazy.js.extensions.0)
1.  [function <span class="apidocSignatureSpan">lazy.js.extensions.</span>1 (source)](#apidoc.element.lazy.js.extensions.1)

#### [module lazy.js.util](#apidoc.module.lazy.js.util)
1.  [function <span class="apidocSignatureSpan">lazy.js.util.</span>isHarmonySupported ()](#apidoc.element.lazy.js.util.isHarmonySupported)



# <a name="apidoc.module.lazy.js"></a>[module lazy.js](#apidoc.module.lazy.js)

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>ArrayLikeSequence ()](#apidoc.element.lazy.js.ArrayLikeSequence)
- description and source-code
```javascript
function ArrayLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncHandle"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>AsyncHandle (cancelFn)](#apidoc.element.lazy.js.AsyncHandle)
- description and source-code
```javascript
function AsyncHandle(cancelFn) {
  this.resolveListeners = [];
  this.rejectListeners = [];
  this.state = PENDING;
  this.cancelFn = cancelFn;
}
```
- example usage
```shell
...
 *     it's read from the stream. Return false from the function to stop reading
 *     the stream.
 */
StreamedSequence.prototype.each = function(fn) {
  var cancelled = false,
  encoding = this.encoding;

  var handle = new Lazy.AsyncHandle(function cancel() { cancelled = true; });

  this.openStream(function(stream) {
if (stream.setEncoding) {
  stream.setEncoding(encoding || 'utf8');
}

var listener = function(e) {
...
```

#### <a name="apidoc.element.lazy.js.AsyncSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>AsyncSequence (parent, interval)](#apidoc.element.lazy.js.AsyncSequence)
- description and source-code
```javascript
function AsyncSequence(parent, interval) {
  if (parent instanceof AsyncSequence) {
    throw new Error("Sequence is already asynchronous!");
  }

  this.parent         = parent;
  this.interval       = interval;
  this.onNextCallback = getOnNextCallback(interval);
  this.cancelCallback = getCancelCallback(interval);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.GeneratedSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.GeneratedSequence)
- description and source-code
```javascript
function GeneratedSequence(generatorFn, length) {
  this.get = generatorFn;
  this.fixedLength = length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>ObjectLikeSequence ()](#apidoc.element.lazy.js.ObjectLikeSequence)
- description and source-code
```javascript
function ObjectLikeSequence() {}
```
- example usage
```shell
...
  /**
   * @constructor
   */
  function MapWrapper(map) {
this.map = map;
  }

  MapWrapper.prototype = new Lazy.ObjectLikeSequence();

  MapWrapper.prototype.each = function each(fn) {
var map = this.map;

for (var pair of map) {
  if (fn(pair[1], pair[0]) === false) {
    return false;
...
```

#### <a name="apidoc.element.lazy.js.Sequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>Sequence ()](#apidoc.element.lazy.js.Sequence)
- description and source-code
```javascript
function Sequence() {}
```
- example usage
```shell
...
  /**
   * @constructor
   */
  function GeneratorWrapper(generator) {
this.generator = generator;
  }

  GeneratorWrapper.prototype = new Lazy.Sequence();

  GeneratorWrapper.prototype.each = function each(fn) {
var iterator = this.generator(),
    result,
    i = 0;

while (!(result = iterator.next()).done) {
...
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>StreamLikeSequence ()](#apidoc.element.lazy.js.StreamLikeSequence)
- description and source-code
```javascript
function StreamLikeSequence() {}
```
- example usage
```shell
...
/**
 * @constructor
 */
function StreamedSequence(stream) {
  this.stream = stream;
}

StreamedSequence.prototype = new Lazy.StreamLikeSequence();

StreamedSequence.prototype.openStream = function(callback) {
  this.stream.resume();
  callback(this.stream);
};

/**
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>StringLikeSequence ()](#apidoc.element.lazy.js.StringLikeSequence)
- description and source-code
```javascript
function StringLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.clone"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>clone (target)](#apidoc.element.lazy.js.clone)
- description and source-code
```javascript
function clone(target) {
  return Lazy(target).value();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.createWrapper"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>createWrapper (initializer)](#apidoc.element.lazy.js.createWrapper)
- description and source-code
```javascript
function createWrapper(initializer) {
  var ctor = function() {
    this.listeners = [];
  };

  ctor.prototype = new StreamLikeSequence();

  ctor.prototype.each = function(listener) {
    this.listeners.push(listener);
  };

  ctor.prototype.emit = function(data) {
    var listeners = this.listeners;

    for (var len = listeners.length, i = len - 1; i >= 0; --i) {
      if (listeners[i](data) === false) {
        listeners.splice(i, 1);
      }
    }
  };

  return function() {
    var sequence = new ctor();
    initializer.apply(sequence, arguments);
    return sequence;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.deprecate"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>deprecate (message, fn)](#apidoc.element.lazy.js.deprecate)
- description and source-code
```javascript
function deprecate(message, fn) {
  return function() {
    console.warn(message);
    return fn.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.generate"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>generate (generatorFn, length)](#apidoc.element.lazy.js.generate)
- description and source-code
```javascript
function generate(generatorFn, length) {
  return new GeneratedSequence(generatorFn, length);
}
```
- example usage
```shell
...
### Indefinite sequence generation

The sequence-based paradigm of Lazy.js lets you do some pretty cool things that simply aren't possible with Underscore's array-based
 approach. One of these is the generation of **indefinite sequences**, which can go on forever, yet still support all of Lazy's
built-in mapping and filtering capabilities.

Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
  .map(function(e) { return Math.floor(e * 1000) + 1; })
  .uniq()
  .take(300)
  .each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).
...
```

#### <a name="apidoc.element.lazy.js.identity"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>identity (x)](#apidoc.element.lazy.js.identity)
- description and source-code
```javascript
function identity(x) { return x; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.isES6Generator"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>isES6Generator (fn)](#apidoc.element.lazy.js.isES6Generator)
- description and source-code
```javascript
function isES6Generator(fn) {
  return fn instanceof GeneratorConstructor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.ArrayLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.ArrayLikeSequence ()](#apidoc.element.lazy.js.js.ArrayLikeSequence)
- description and source-code
```javascript
function ArrayLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.AsyncHandle"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncHandle (cancelFn)](#apidoc.element.lazy.js.js.AsyncHandle)
- description and source-code
```javascript
function AsyncHandle(cancelFn) {
  this.resolveListeners = [];
  this.rejectListeners = [];
  this.state = PENDING;
  this.cancelFn = cancelFn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.AsyncSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.AsyncSequence (parent, interval)](#apidoc.element.lazy.js.js.AsyncSequence)
- description and source-code
```javascript
function AsyncSequence(parent, interval) {
  if (parent instanceof AsyncSequence) {
    throw new Error("Sequence is already asynchronous!");
  }

  this.parent         = parent;
  this.interval       = interval;
  this.onNextCallback = getOnNextCallback(interval);
  this.cancelCallback = getCancelCallback(interval);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.GeneratedSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.js.GeneratedSequence)
- description and source-code
```javascript
function GeneratedSequence(generatorFn, length) {
  this.get = generatorFn;
  this.fixedLength = length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.ObjectLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.ObjectLikeSequence ()](#apidoc.element.lazy.js.js.ObjectLikeSequence)
- description and source-code
```javascript
function ObjectLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.Sequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.Sequence ()](#apidoc.element.lazy.js.js.Sequence)
- description and source-code
```javascript
function Sequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.StreamLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.StreamLikeSequence ()](#apidoc.element.lazy.js.js.StreamLikeSequence)
- description and source-code
```javascript
function StreamLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.js.StringLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>js.StringLikeSequence ()](#apidoc.element.lazy.js.js.StringLikeSequence)
- description and source-code
```javascript
function StringLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.makeHttpRequest"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>makeHttpRequest (url)](#apidoc.element.lazy.js.makeHttpRequest)
- description and source-code
```javascript
makeHttpRequest = function (url) {
  return new HttpStreamSequence(url);
}
```
- example usage
```shell
...
// Read the first 5 lines from a file:
Lazy.readFile("path/to/file")
  .lines()
  .take(5)
  .each(doSomething);

// Read lines 5-10 from an HTTP response.
Lazy.makeHttpRequest("http://example.com")
  .lines()
  .drop(5)
  .take(5)
  .each(doSomething);
'''

In each case, the elements in the sequence will be "chunks" of data most likely comprising multiple lines. The 'lines()' method
splits each chunk into lines (lazily, of course).
...
```

#### <a name="apidoc.element.lazy.js.noop"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>noop ()](#apidoc.element.lazy.js.noop)
- description and source-code
```javascript
function noop() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.parseJSON"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>parseJSON (json)](#apidoc.element.lazy.js.parseJSON)
- description and source-code
```javascript
parseJSON = function (json) {
  return new JsonSequence(json);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.range"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>range ()](#apidoc.element.lazy.js.range)
- description and source-code
```javascript
function range() {
  var start = arguments.length > 1 ? arguments[0] : 0,
      stop  = arguments.length > 1 ? arguments[1] : arguments[0],
      step  = arguments.length > 2 && arguments[2];

  if (step === false) {
    step = stop > start ? 1 : -1;
  }

  if (step === 0) {
    return Lazy([]);
  }

  return Lazy.generate(function(i) { return start + (step * i); })
    .take(Math.ceil((stop - start) / step));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.readFile"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>readFile (path, encoding)](#apidoc.element.lazy.js.readFile)
- description and source-code
```javascript
readFile = function (path, encoding) {
  return new FileStreamSequence(path, encoding);
}
```
- example usage
```shell
...
.each(processData);
'''

For convenience, specialized helper methods for dealing with either file streams or HTTP streams are also offered. (**Note: this
 API will probably change.**)

'''javascript
// Read the first 5 lines from a file:
Lazy.readFile("path/to/file")
.lines()
.take(5)
.each(doSomething);

// Read lines 5-10 from an HTTP response.
Lazy.makeHttpRequest("http://example.com")
.lines()
...
```

#### <a name="apidoc.element.lazy.js.repeat"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>repeat (value, count)](#apidoc.element.lazy.js.repeat)
- description and source-code
```javascript
function repeat(value, count) {
  return Lazy.generate(function() { return value; }, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.strict"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>strict ()](#apidoc.element.lazy.js.strict)
- description and source-code
```javascript
function strict() {
  function StrictLazy(source) {
    if (source == null) {
      throw new Error("You cannot wrap null or undefined using Lazy.");
    }

    if (typeof source === "number" || typeof source === "boolean") {
      throw new Error("You cannot wrap primitive values using Lazy.");
    }

    return Lazy(source);
  };

  Lazy(Lazy).each(function(property, name) {
    StrictLazy[name] = property;
  });

  return StrictLazy;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.ArrayLikeSequence"></a>[module lazy.js.ArrayLikeSequence](#apidoc.module.lazy.js.ArrayLikeSequence)

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.ArrayLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>ArrayLikeSequence ()](#apidoc.element.lazy.js.ArrayLikeSequence.ArrayLikeSequence)
- description and source-code
```javascript
function ArrayLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.define"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.ArrayLikeSequence.define)
- description and source-code
```javascript
function define(methodName, overrides) {
  if (!overrides || typeof overrides.get !== 'function') {
    throw new Error("A custom array-like sequence must implement *at least* get!");
  }

  return defineSequenceType(ArrayLikeSequence, methodName, overrides);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.ArrayLikeSequence.prototype"></a>[module lazy.js.ArrayLikeSequence.prototype](#apidoc.module.lazy.js.ArrayLikeSequence.prototype)

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.concat"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>concat (var_args)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.concat)
- description and source-code
```javascript
function concat(var_args) {
  if (arguments.length === 1 && isArray(arguments[0])) {
    return new IndexedConcatenatedSequence(this, (/** @type {Array} */ var_args));
  } else {
    return Sequence.prototype.concat.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.each"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.each)
- description and source-code
```javascript
function each(fn) {
  var length = this.length(),
      i = -1;

  while (++i < length) {
    if (fn(this.get(i), i) === false) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
...
Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
.map(function(e) { return Math.floor(e * 1000) + 1; })
.uniq()
.take(300)
.each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
var fibonacci = Lazy.generate(function() {
var x = 1,
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.filter"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.filter)
- description and source-code
```javascript
function filter(filterFn) {
  return new IndexedFilteredSequence(this, createCallback(filterFn));
}
```
- example usage
```shell
...
'''

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.first"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>first (count)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.first)
- description and source-code
```javascript
function first(count) {
  if (typeof count === "undefined") {
    return this.get(0);
  }

  return new IndexedTakeSequence(this, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.get"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>get (i)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.get)
- description and source-code
```javascript
function get(i) {
  return this.parent.get(i);
}
```
- example usage
```shell
...
 this.url = url;
 this.encoding = encoding;
}

HttpStreamSequence.prototype = new StreamedSequence();

HttpStreamSequence.prototype.openStream = function(callback) {
 http.get(URL.parse(this.url), callback);
};

/**
* Creates a {@link Sequence} from an HTTP stream, whose elements are chunks of
* data as the stream is read. This sequence works asynchronously, so
* synchronous methods such as {@code indexOf}, {@code any}, and {@code toArray}
* won't work.
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIndex"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>getIndex ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIndex)
- description and source-code
```javascript
function getIndex() {
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIterator"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.getIterator)
- description and source-code
```javascript
function getIterator() {
  return new IndexedIterator(this);
}
```
- example usage
```shell
...

  if (typeof Lazy === 'undefined' && typeof require === 'function') {
Lazy = require('../lazy.js');
  }

  if (typeof Symbol !== 'undefined') {
Lazy.Sequence.prototype[Symbol.iterator] = function() {
  return new IteratorAdapter(this.getIterator());
}

function IteratorAdapter(iterator) {
  this.iterator = iterator;
}

IteratorAdapter.prototype.next = function next() {
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.length"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>length ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.length)
- description and source-code
```javascript
function length() {
  return this.parent.length();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.map"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>map (mapFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.map)
- description and source-code
```javascript
function map(mapFn) {
  return new IndexedMappedSequence(this, createCallback(mapFn));
}
```
- example usage
```shell
...

The sequence-based paradigm of Lazy.js lets you do some pretty cool things that simply aren't possible with Underscore's array-based
 approach. One of these is the generation of **indefinite sequences**, which can go on forever, yet still support all of Lazy's
built-in mapping and filtering capabilities.

Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
  .map(function(e) { return Math.floor(e * 1000) + 1; })
  .uniq()
  .take(300)
  .each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.pop"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>pop ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.pop)
- description and source-code
```javascript
function pop() {
  return this.initial();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.push"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>push (value)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.push)
- description and source-code
```javascript
function push(value) {
  return this.concat([value]);
}
```
- example usage
```shell
...

So if performance and/or efficiency were a concern for you, you would probably *not* do things that way using Underscore. Instead
, you'd likely go the procedural route:

'''javascript
var results = [];
for (var i = 0; i < people.length; ++i) {
  if (people[i].lastName.startsWith('Smith')) {
    results.push(people[i].lastName);
    if (results.length === 5) {
      break;
    }
  }
}
'''
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.rest"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>rest (count)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.rest)
- description and source-code
```javascript
function rest(count) {
  return new IndexedDropSequence(this, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.reverse"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.reverse)
- description and source-code
```javascript
function reverse() {
  return new IndexedReversedSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.shift"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>shift ()](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.shift)
- description and source-code
```javascript
function shift() {
  return this.drop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.slice"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>slice (begin, end)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.slice)
- description and source-code
```javascript
function slice(begin, end) {
  var length = this.length();

  if (begin < 0) {
    begin = length + begin;
  }

  var result = this.drop(begin);

  if (typeof end === "number") {
    if (end < 0) {
      end = length + end;
    }
    result = result.take(end - begin);
  }

  return result;
}
```
- example usage
```shell
...
### String processing

Now here's something you may not have even thought of: 'String.match' and 'String.split'. In JavaScript, each of these methods returns
 an *array* of substrings. If you think about it, this often means doing more work than necessary; but it's the quickest way (from
 a developer's standpoint) to get the job done.

For example, suppose you wanted the first five lines of a block of text. You could always do this:

'''javascript
var firstFiveLines = text.split("\n").slice(0, 5);
'''

But of course, this actually splits *the entire string* into every single line. If the string is very large, this is quite wasteful
.

With Lazy.js, we don't need to split up an entire string just to treat it as a sequence of lines. We can get the same effect by
wrapping the string with 'Lazy' and calling 'split':

'''javascript
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.uniq"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>uniq (keyFn)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.uniq)
- description and source-code
```javascript
function uniq(keyFn) {
  return new IndexedUniqueSequence(this, createCallback(keyFn));
}
```
- example usage
```shell
...
The sequence-based paradigm of Lazy.js lets you do some pretty cool things that simply aren't possible with Underscore's array-based
 approach. One of these is the generation of **indefinite sequences**, which can go on forever, yet still support all of Lazy's
built-in mapping and filtering capabilities.

Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
  .map(function(e) { return Math.floor(e * 1000) + 1; })
  .uniq()
  .take(300)
  .each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
...
```

#### <a name="apidoc.element.lazy.js.ArrayLikeSequence.prototype.unshift"></a>[function <span class="apidocSignatureSpan">lazy.js.ArrayLikeSequence.prototype.</span>unshift (value)](#apidoc.element.lazy.js.ArrayLikeSequence.prototype.unshift)
- description and source-code
```javascript
function unshift(value) {
  return Lazy([value]).concat(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.AsyncHandle"></a>[module lazy.js.AsyncHandle](#apidoc.module.lazy.js.AsyncHandle)

#### <a name="apidoc.element.lazy.js.AsyncHandle.AsyncHandle"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>AsyncHandle (cancelFn)](#apidoc.element.lazy.js.AsyncHandle.AsyncHandle)
- description and source-code
```javascript
function AsyncHandle(cancelFn) {
  this.resolveListeners = [];
  this.rejectListeners = [];
  this.state = PENDING;
  this.cancelFn = cancelFn;
}
```
- example usage
```shell
...
 *     it's read from the stream. Return false from the function to stop reading
 *     the stream.
 */
StreamedSequence.prototype.each = function(fn) {
  var cancelled = false,
  encoding = this.encoding;

  var handle = new Lazy.AsyncHandle(function cancel() { cancelled = true; });

  this.openStream(function(stream) {
if (stream.setEncoding) {
  stream.setEncoding(encoding || 'utf8');
}

var listener = function(e) {
...
```



# <a name="apidoc.module.lazy.js.AsyncHandle.prototype"></a>[module lazy.js.AsyncHandle.prototype](#apidoc.module.lazy.js.AsyncHandle.prototype)

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype._reject"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>_reject (reason)](#apidoc.element.lazy.js.AsyncHandle.prototype._reject)
- description and source-code
```javascript
function _reject(reason) {
  if (this.state === RESOLVED) {
    return;
  }

  if (this.state === PENDING) {
    this.state = REJECTED;
    this.reason = reason;
  }

  consumeListeners(this.rejectListeners, this.reason);
}
```
- example usage
```shell
...
var listener = function(e) {
  try {
    if (cancelled || fn(e) === false) {
      stream.removeListener("data", listener);
      handle._resolve(false);
    }
  } catch (e) {
    handle._reject(e);
  }
};

stream.on("data", listener);

stream.on("end", function() {
  handle._resolve(true);
...
```

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype._resolve"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>_resolve (value)](#apidoc.element.lazy.js.AsyncHandle.prototype._resolve)
- description and source-code
```javascript
function _resolve(value) {
  if (this.state === REJECTED) {
    return;
  }

  if (this.state === PENDING) {
    this.state = RESOLVED;
    this.value = value;
  }

  consumeListeners(this.resolveListeners, this.value);
}
```
- example usage
```shell
...
  stream.setEncoding(encoding || 'utf8');
}

var listener = function(e) {
  try {
    if (cancelled || fn(e) === false) {
      stream.removeListener("data", listener);
      handle._resolve(false);
    }
  } catch (e) {
    handle._reject(e);
  }
};

stream.on("data", listener);
...
```

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype.cancel"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>cancel ()](#apidoc.element.lazy.js.AsyncHandle.prototype.cancel)
- description and source-code
```javascript
function cancel() {
  if (this.cancelFn) {
    this.cancelFn();
    this.cancelFn = null;
    this._resolve(false);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype.onComplete"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>onComplete (callback)](#apidoc.element.lazy.js.AsyncHandle.prototype.onComplete)
- description and source-code
```javascript
function onComplete(callback) {
  this.resolveListeners.push(callback);
  return this;
}
```
- example usage
```shell
...
      var handle = this.sequence.each(function(line, i) {
        if (self.delimiter != null) {
          line += self.delimiter;
        }
        return self.push(line, i);
      });
      if (handle instanceof Lazy.AsyncHandle) {
        handle.onComplete(function() {
          self.push(null);
        });
      }
      this.started = true;
    }
  };
}
...
```

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype.onError"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>onError (callback)](#apidoc.element.lazy.js.AsyncHandle.prototype.onError)
- description and source-code
```javascript
function onError(callback) {
  this.rejectListeners.push(callback);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncHandle.prototype.then"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncHandle.prototype.</span>then (onFulfilled, onRejected)](#apidoc.element.lazy.js.AsyncHandle.prototype.then)
- description and source-code
```javascript
function then(onFulfilled, onRejected) {
  var promise = new AsyncHandle(this.cancelFn);

  this.resolveListeners.push(function(value) {
    try {
      if (typeof onFulfilled !== 'function') {
        resolve(promise, value);
        return;
      }

      resolve(promise, onFulfilled(value));

    } catch (e) {
      promise._reject(e);
    }
  });

  this.rejectListeners.push(function(reason) {
    try {
      if (typeof onRejected !== 'function') {
        promise._reject(reason);
        return;
      }

      resolve(promise, onRejected(reason));

    } catch (e) {
      promise._reject(e);
    }
  });

  if (this.state === RESOLVED) {
    this._resolve(this.value);
  }

  if (this.state === REJECTED) {
    this._reject(this.reason);
  }

  return promise;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.AsyncSequence"></a>[module lazy.js.AsyncSequence](#apidoc.module.lazy.js.AsyncSequence)

#### <a name="apidoc.element.lazy.js.AsyncSequence.AsyncSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>AsyncSequence (parent, interval)](#apidoc.element.lazy.js.AsyncSequence.AsyncSequence)
- description and source-code
```javascript
function AsyncSequence(parent, interval) {
  if (parent instanceof AsyncSequence) {
    throw new Error("Sequence is already asynchronous!");
  }

  this.parent         = parent;
  this.interval       = interval;
  this.onNextCallback = getOnNextCallback(interval);
  this.cancelCallback = getCancelCallback(interval);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.AsyncSequence.prototype"></a>[module lazy.js.AsyncSequence.prototype](#apidoc.module.lazy.js.AsyncSequence.prototype)

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.async"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>async ()](#apidoc.element.lazy.js.AsyncSequence.prototype.async)
- description and source-code
```javascript
function async() {
  return this;
}
```
- example usage
```shell
...

### Asynchronous iteration

You've probably [seen code snippets before](https://gist.github.com/dtao/2351944) that show how to iterate over an array asynchronously
 in JavaScript. But have you seen an example with functional goodness like this?

'''javascript
Lazy.generate(Lazy.identity)
  .async(1000) // specifies a 1-second interval between each element
  .map(function(x) { return String.fromCharCode(x + 65); })
  .take(26)
  .each(function(char) { console.log(char); });
'''

All right... what else?
...
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.contains"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>contains (value)](#apidoc.element.lazy.js.AsyncSequence.prototype.contains)
- description and source-code
```javascript
function contains(value) {
  var found = false;

  var handle = this.each(function(e) {
    if (e === value) {
      found = true;
      return false;
    }
  });

  return handle.then(function() {
    return found;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.each"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.AsyncSequence.prototype.each)
- description and source-code
```javascript
function each(fn) {
  var iterator = this.parent.getIterator(),
      onNextCallback = this.onNextCallback,
      cancelCallback = this.cancelCallback,
      i = 0;

  var handle = new AsyncHandle(function cancel() {
    if (cancellationId) {
      cancelCallback(cancellationId);
    }
  });

  var cancellationId = onNextCallback(function iterate() {
    cancellationId = null;

    try {
      if (iterator.moveNext() && fn(iterator.current(), i++) !== false) {
        cancellationId = onNextCallback(iterate);

      } else {
        handle._resolve();
      }

    } catch (e) {
      handle._reject(e);
    }
  });

  return handle;
}
```
- example usage
```shell
...
Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
.map(function(e) { return Math.floor(e * 1000) + 1; })
.uniq()
.take(300)
.each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
var fibonacci = Lazy.generate(function() {
var x = 1,
...
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.find"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>find (predicate)](#apidoc.element.lazy.js.AsyncSequence.prototype.find)
- description and source-code
```javascript
function find(predicate) {
  var found;

  var handle = this.each(function(e, i) {
    if (predicate(e, i)) {
      found = e;
      return false;
    }
  });

  return handle.then(function() { return found; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.getIterator"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.AsyncSequence.prototype.getIterator)
- description and source-code
```javascript
function getIterator() {
  throw new Error('An AsyncSequence does not support synchronous iteration.');
}
```
- example usage
```shell
...

  if (typeof Lazy === 'undefined' && typeof require === 'function') {
Lazy = require('../lazy.js');
  }

  if (typeof Symbol !== 'undefined') {
Lazy.Sequence.prototype[Symbol.iterator] = function() {
  return new IteratorAdapter(this.getIterator());
}

function IteratorAdapter(iterator) {
  this.iterator = iterator;
}

IteratorAdapter.prototype.next = function next() {
...
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>indexOf (value)](#apidoc.element.lazy.js.AsyncSequence.prototype.indexOf)
- description and source-code
```javascript
function indexOf(value) {
  var foundIndex = -1;

  var handle = this.each(function(e, i) {
    if (e === value) {
      foundIndex = i;
      return false;
    }
  });

  return handle.then(function() {
    return foundIndex;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.isAsync"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.AsyncSequence.prototype.isAsync)
- description and source-code
```javascript
function isAsync() {
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.AsyncSequence.prototype.reverse"></a>[function <span class="apidocSignatureSpan">lazy.js.AsyncSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.AsyncSequence.prototype.reverse)
- description and source-code
```javascript
function reverse() {
  return this.parent.reverse().async();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.GeneratedSequence"></a>[module lazy.js.GeneratedSequence](#apidoc.module.lazy.js.GeneratedSequence)

#### <a name="apidoc.element.lazy.js.GeneratedSequence.GeneratedSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>GeneratedSequence (generatorFn, length)](#apidoc.element.lazy.js.GeneratedSequence.GeneratedSequence)
- description and source-code
```javascript
function GeneratedSequence(generatorFn, length) {
  this.get = generatorFn;
  this.fixedLength = length;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.GeneratedSequence.prototype"></a>[module lazy.js.GeneratedSequence.prototype](#apidoc.module.lazy.js.GeneratedSequence.prototype)

#### <a name="apidoc.element.lazy.js.GeneratedSequence.prototype.each"></a>[function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.GeneratedSequence.prototype.each)
- description and source-code
```javascript
function each(fn) {
  var generatorFn = this.get,
      length = this.fixedLength,
      i = 0;

  while (typeof length === "undefined" || i < length) {
    if (fn(generatorFn(i), i++) === false) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
...
Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
.map(function(e) { return Math.floor(e * 1000) + 1; })
.uniq()
.take(300)
.each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
var fibonacci = Lazy.generate(function() {
var x = 1,
...
```

#### <a name="apidoc.element.lazy.js.GeneratedSequence.prototype.getIterator"></a>[function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.getIterator)
- description and source-code
```javascript
function getIterator() {
  return new GeneratedIterator(this);
}
```
- example usage
```shell
...

  if (typeof Lazy === 'undefined' && typeof require === 'function') {
Lazy = require('../lazy.js');
  }

  if (typeof Symbol !== 'undefined') {
Lazy.Sequence.prototype[Symbol.iterator] = function() {
  return new IteratorAdapter(this.getIterator());
}

function IteratorAdapter(iterator) {
  this.iterator = iterator;
}

IteratorAdapter.prototype.next = function next() {
...
```

#### <a name="apidoc.element.lazy.js.GeneratedSequence.prototype.isAsync"></a>[function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.isAsync)
- description and source-code
```javascript
function isAsync() {
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.GeneratedSequence.prototype.length"></a>[function <span class="apidocSignatureSpan">lazy.js.GeneratedSequence.prototype.</span>length ()](#apidoc.element.lazy.js.GeneratedSequence.prototype.length)
- description and source-code
```javascript
function length() {
  return this.fixedLength;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.ObjectLikeSequence"></a>[module lazy.js.ObjectLikeSequence](#apidoc.module.lazy.js.ObjectLikeSequence)

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.ObjectLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>ObjectLikeSequence ()](#apidoc.element.lazy.js.ObjectLikeSequence.ObjectLikeSequence)
- description and source-code
```javascript
function ObjectLikeSequence() {}
```
- example usage
```shell
...
  /**
   * @constructor
   */
  function MapWrapper(map) {
this.map = map;
  }

  MapWrapper.prototype = new Lazy.ObjectLikeSequence();

  MapWrapper.prototype.each = function each(fn) {
var map = this.map;

for (var pair of map) {
  if (fn(pair[1], pair[0]) === false) {
    return false;
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.define"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.ObjectLikeSequence.define)
- description and source-code
```javascript
function define(methodName, overrides) {
  if (!overrides || typeof overrides.each !== 'function') {
    throw new Error("A custom object-like sequence must implement *at least* each!");
  }

  return defineSequenceType(ObjectLikeSequence, methodName, overrides);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.ObjectLikeSequence.prototype"></a>[module lazy.js.ObjectLikeSequence.prototype](#apidoc.module.lazy.js.ObjectLikeSequence.prototype)

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.assign"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>assign (other)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.assign)
- description and source-code
```javascript
function assign(other) {
  return new AssignSequence(this, other);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.async"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>async ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.async)
- description and source-code
```javascript
function async() {
  throw new Error('An ObjectLikeSequence does not support asynchronous iteration.');
}
```
- example usage
```shell
...

### Asynchronous iteration

You've probably [seen code snippets before](https://gist.github.com/dtao/2351944) that show how to iterate over an array asynchronously
 in JavaScript. But have you seen an example with functional goodness like this?

'''javascript
Lazy.generate(Lazy.identity)
  .async(1000) // specifies a 1-second interval between each element
  .map(function(x) { return String.fromCharCode(x + 65); })
  .take(26)
  .each(function(char) { console.log(char); });
'''

All right... what else?
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.defaults"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>defaults (defaults)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.defaults)
- description and source-code
```javascript
function defaults(defaults) {
  return new DefaultsSequence(this, defaults);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.extend"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>extend (other)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.extend)
- description and source-code
```javascript
function extend(other) {
  return this.assign(other);
}
```
- example usage
```shell
...

  Lazy.Sequence.prototype.pipe = function pipe(destination) {
this.toStream().pipe(destination);
  };

  function LazyStream(sequence, options) {
options = Lazy(options || {})
  .extend({ objectMode: true })
  .toObject();

Stream.Readable.call(this, options);

this.sequence = sequence;
this.started  = false;
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.filter"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.filter)
- description and source-code
```javascript
function filter(filterFn) {
  return new FilteredObjectLikeSequence(this, createCallback(filterFn));
}
```
- example usage
```shell
...
'''

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.functions"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>functions ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.functions)
- description and source-code
```javascript
function functions() {
  return this
    .filter(function(v, k) { return typeof(v) === "function"; })
    .map(function(v, k) { return k; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.get"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>get (key)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.get)
- description and source-code
```javascript
function get(key) {
  var pair = this.pairs().find(function(pair) {
    return pair[0] === key;
  });

  return pair ? pair[1] : undefined;
}
```
- example usage
```shell
...
 this.url = url;
 this.encoding = encoding;
}

HttpStreamSequence.prototype = new StreamedSequence();

HttpStreamSequence.prototype.openStream = function(callback) {
 http.get(URL.parse(this.url), callback);
};

/**
* Creates a {@link Sequence} from an HTTP stream, whose elements are chunks of
* data as the stream is read. This sequence works asynchronously, so
* synchronous methods such as {@code indexOf}, {@code any}, and {@code toArray}
* won't work.
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.invert"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>invert ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.invert)
- description and source-code
```javascript
function invert() {
  return new InvertedSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.keys"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>keys ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.keys)
- description and source-code
```javascript
function keys() {
  return new KeySequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.merge"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>merge (var_args)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.merge)
- description and source-code
```javascript
function merge(var_args) {
  var mergeFn = arguments.length > 1 && typeof arguments[arguments.length - 1] === "function" ?
    arrayPop.call(arguments) : null;
  return new MergedSequence(this, arraySlice.call(arguments, 0), mergeFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.methods"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>methods ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.methods)
- description and source-code
```javascript
function methods() {
  return this.functions();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.omit"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>omit (properties)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.omit)
- description and source-code
```javascript
function omit(properties) {
  return new OmitSequence(this, properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.pairs"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>pairs ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.pairs)
- description and source-code
```javascript
function pairs() {
  return this.map(function(v, k) { return [k, v]; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.pick"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>pick (properties)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.pick)
- description and source-code
```javascript
function pick(properties) {
  return new PickSequence(this, properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.reverse"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.reverse)
- description and source-code
```javascript
function reverse() {
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.toArray"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>toArray ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.toArray)
- description and source-code
```javascript
function toArray() {
  return this.pairs().toArray();
}
```
- example usage
```shell
...
    x = y;
    y += prev;
    return prev;
  };
}());

// Output: [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
fibonacci.take(10).toArray();
'''

OK, what else?

### Asynchronous iteration

You've probably [seen code snippets before](https://gist.github.com/dtao/2351944) that show how to iterate over an array asynchronously
 in JavaScript. But have you seen an example with functional goodness like this?
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.toObject"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>toObject ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.toObject)
- description and source-code
```javascript
function toObject() {
  return this.reduce(function(object, value, key) {
    object[key] = value;
    return object;
  }, {});
}
```
- example usage
```shell
...
  Lazy.Sequence.prototype.pipe = function pipe(destination) {
this.toStream().pipe(destination);
  };

  function LazyStream(sequence, options) {
options = Lazy(options || {})
  .extend({ objectMode: true })
  .toObject();

Stream.Readable.call(this, options);

this.sequence = sequence;
this.started  = false;

// Find delimiter on a (parent) sequence object if set
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.value"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>value ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.value)
- description and source-code
```javascript
function value() {
  return this.toObject();
}
```
- example usage
```shell
...
Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
- 'filter(...)': iterates over the new array, creating yet *another* (potentially giant) array
- 'take(5)': all that just for 5 elements!
...
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.values"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>values ()](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.values)
- description and source-code
```javascript
function values() {
  return new ValuesSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.ObjectLikeSequence.prototype.watch"></a>[function <span class="apidocSignatureSpan">lazy.js.ObjectLikeSequence.prototype.</span>watch (propertyNames)](#apidoc.element.lazy.js.ObjectLikeSequence.prototype.watch)
- description and source-code
```javascript
function watch(propertyNames) {
  throw new Error('You can only call #watch on a directly wrapped object.');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.Sequence"></a>[module lazy.js.Sequence](#apidoc.module.lazy.js.Sequence)

#### <a name="apidoc.element.lazy.js.Sequence.Sequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>Sequence ()](#apidoc.element.lazy.js.Sequence.Sequence)
- description and source-code
```javascript
function Sequence() {}
```
- example usage
```shell
...
  /**
   * @constructor
   */
  function GeneratorWrapper(generator) {
this.generator = generator;
  }

  GeneratorWrapper.prototype = new Lazy.Sequence();

  GeneratorWrapper.prototype.each = function each(fn) {
var iterator = this.generator(),
    result,
    i = 0;

while (!(result = iterator.next()).done) {
...
```

#### <a name="apidoc.element.lazy.js.Sequence.define"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.Sequence.define)
- description and source-code
```javascript
function define(methodName, overrides) {
  if (!overrides || (!overrides.getIterator && !overrides.each)) {
    throw new Error("A custom sequence must implement *at least* getIterator or each!");
  }

  return defineSequenceType(Sequence, methodName, overrides);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.Sequence.prototype"></a>[module lazy.js.Sequence.prototype](#apidoc.module.lazy.js.Sequence.prototype)

#### <a name="apidoc.element.lazy.js.Sequence.prototype.all"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>all (predicate)](#apidoc.element.lazy.js.Sequence.prototype.all)
- description and source-code
```javascript
function all(predicate) {
  return this.every(predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.any"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>any (predicate)](#apidoc.element.lazy.js.Sequence.prototype.any)
- description and source-code
```javascript
function any(predicate) {
  return this.some(predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.apply"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>apply (source)](#apidoc.element.lazy.js.Sequence.prototype.apply)
- description and source-code
```javascript
function apply(source) {
  var root = this.root(),
      previousSource = root.source,
      result;

  try {
    root.source = source;
    result = this.value();
  } finally {
    root.source = previousSource;
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.async"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>async (interval)](#apidoc.element.lazy.js.Sequence.prototype.async)
- description and source-code
```javascript
function async(interval) {
  return new AsyncSequence(this, interval);
}
```
- example usage
```shell
...

### Asynchronous iteration

You've probably [seen code snippets before](https://gist.github.com/dtao/2351944) that show how to iterate over an array asynchronously
 in JavaScript. But have you seen an example with functional goodness like this?

'''javascript
Lazy.generate(Lazy.identity)
  .async(1000) // specifies a 1-second interval between each element
  .map(function(x) { return String.fromCharCode(x + 65); })
  .take(26)
  .each(function(char) { console.log(char); });
'''

All right... what else?
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.chunk"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>chunk (size)](#apidoc.element.lazy.js.Sequence.prototype.chunk)
- description and source-code
```javascript
function chunk(size) {
  if (size < 1) {
    throw new Error("You must specify a positive chunk size.");
  }

  return new ChunkedSequence(this, size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.collect"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>collect (mapFn)](#apidoc.element.lazy.js.Sequence.prototype.collect)
- description and source-code
```javascript
function collect(mapFn) {
  return this.map(mapFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.compact"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>compact ()](#apidoc.element.lazy.js.Sequence.prototype.compact)
- description and source-code
```javascript
function compact() {
  return this.filter(function(e) { return !!e; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.concat"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>concat (var_args)](#apidoc.element.lazy.js.Sequence.prototype.concat)
- description and source-code
```javascript
function concat(var_args) {
  return new ConcatenatedSequence(this, arraySlice.call(arguments, 0));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.consecutive"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>consecutive (count)](#apidoc.element.lazy.js.Sequence.prototype.consecutive)
- description and source-code
```javascript
function consecutive(count) {
  var queue    = new Queue(count);
  var segments = this.map(function(element) {
    if (queue.add(element).count === count) {
      return queue.toArray();
    }
  });
  return segments.compact();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.contains"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>contains (value)](#apidoc.element.lazy.js.Sequence.prototype.contains)
- description and source-code
```javascript
function contains(value) {
  return this.indexOf(value) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.countBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>countBy (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.countBy)
- description and source-code
```javascript
function countBy(keyFn) {
  return new CountedSequence(this, keyFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.detect"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>detect (predicate)](#apidoc.element.lazy.js.Sequence.prototype.detect)
- description and source-code
```javascript
function detect(predicate) {
  return this.find(predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.difference"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>difference (var_args)](#apidoc.element.lazy.js.Sequence.prototype.difference)
- description and source-code
```javascript
function difference(var_args) {
  return this.without.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.drop"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>drop (count)](#apidoc.element.lazy.js.Sequence.prototype.drop)
- description and source-code
```javascript
function drop(count) {
  return this.rest(count);
}
```
- example usage
```shell
...
  .lines()
  .take(5)
  .each(doSomething);

// Read lines 5-10 from an HTTP response.
Lazy.makeHttpRequest("http://example.com")
  .lines()
  .drop(5)
  .take(5)
  .each(doSomething);
'''

In each case, the elements in the sequence will be "chunks" of data most likely comprising multiple lines. The 'lines()' method
splits each chunk into lines (lazily, of course).

***
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.dropWhile"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>dropWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.dropWhile)
- description and source-code
```javascript
function dropWhile(predicate) {
  return new DropWhileSequence(this, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.each"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>each (fn)](#apidoc.element.lazy.js.Sequence.prototype.each)
- description and source-code
```javascript
function each(fn) {
  var iterator = this.getIterator(),
      i = -1;

  while (iterator.moveNext()) {
    if (fn(iterator.current(), ++i) === false) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
...
Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
.map(function(e) { return Math.floor(e * 1000) + 1; })
.uniq()
.take(300)
.each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
var fibonacci = Lazy.generate(function() {
var x = 1,
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.every"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>every (predicate)](#apidoc.element.lazy.js.Sequence.prototype.every)
- description and source-code
```javascript
function every(predicate) {
  predicate = createCallback(predicate);

  return this.each(function(e, i) {
    return !!predicate(e, i);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.filter"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>filter (filterFn)](#apidoc.element.lazy.js.Sequence.prototype.filter)
- description and source-code
```javascript
function filter(filterFn) {
  return new FilteredSequence(this, createCallback(filterFn));
}
```
- example usage
```shell
...
'''

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.find"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>find (predicate)](#apidoc.element.lazy.js.Sequence.prototype.find)
- description and source-code
```javascript
function find(predicate) {
  return this.filter(predicate).first();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.findWhere"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>findWhere (properties)](#apidoc.element.lazy.js.Sequence.prototype.findWhere)
- description and source-code
```javascript
function findWhere(properties) {
  return this.where(properties).first();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.first"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>first (count)](#apidoc.element.lazy.js.Sequence.prototype.first)
- description and source-code
```javascript
function first(count) {
  if (typeof count === "undefined") {
    return getFirst(this);
  }
  return new TakeSequence(this, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.flatten"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>flatten ()](#apidoc.element.lazy.js.Sequence.prototype.flatten)
- description and source-code
```javascript
function flatten() {
  return new FlattenedSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.foldl"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>foldl (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.foldl)
- description and source-code
```javascript
function foldl(aggregator, memo) {
  return this.reduce(aggregator, memo);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.foldr"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>foldr (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.foldr)
- description and source-code
```javascript
function foldr(aggregator, memo) {
  return this.reduceRight(aggregator, memo);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.forEach"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>forEach (fn)](#apidoc.element.lazy.js.Sequence.prototype.forEach)
- description and source-code
```javascript
function forEach(fn) {
  return this.each(fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.get"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>get (i)](#apidoc.element.lazy.js.Sequence.prototype.get)
- description and source-code
```javascript
function get(i) {
  var element;
  this.each(function(e, index) {
    if (index === i) {
      element = e;
      return false;
    }
  });
  return element;
}
```
- example usage
```shell
...
 this.url = url;
 this.encoding = encoding;
}

HttpStreamSequence.prototype = new StreamedSequence();

HttpStreamSequence.prototype.openStream = function(callback) {
 http.get(URL.parse(this.url), callback);
};

/**
* Creates a {@link Sequence} from an HTTP stream, whose elements are chunks of
* data as the stream is read. This sequence works asynchronously, so
* synchronous methods such as {@code indexOf}, {@code any}, and {@code toArray}
* won't work.
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.getIndex"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>getIndex ()](#apidoc.element.lazy.js.Sequence.prototype.getIndex)
- description and source-code
```javascript
function getIndex() {
  return new ArrayWrapper(this.toArray());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.getIterator"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.Sequence.prototype.getIterator)
- description and source-code
```javascript
function getIterator() {
  return new Iterator(this);
}
```
- example usage
```shell
...

  if (typeof Lazy === 'undefined' && typeof require === 'function') {
Lazy = require('../lazy.js');
  }

  if (typeof Symbol !== 'undefined') {
Lazy.Sequence.prototype[Symbol.iterator] = function() {
  return new IteratorAdapter(this.getIterator());
}

function IteratorAdapter(iterator) {
  this.iterator = iterator;
}

IteratorAdapter.prototype.next = function next() {
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.groupBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>groupBy (keyFn, valFn)](#apidoc.element.lazy.js.Sequence.prototype.groupBy)
- description and source-code
```javascript
function groupBy(keyFn, valFn) {
  return new GroupedSequence(this, keyFn, valFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.head"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>head (count)](#apidoc.element.lazy.js.Sequence.prototype.head)
- description and source-code
```javascript
head = function (count) {
  return this.first(count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.indexBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>indexBy (keyFn, valFn)](#apidoc.element.lazy.js.Sequence.prototype.indexBy)
- description and source-code
```javascript
indexBy = function (keyFn, valFn) {
  return new IndexedSequence(this, keyFn, valFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>indexOf (value)](#apidoc.element.lazy.js.Sequence.prototype.indexOf)
- description and source-code
```javascript
function indexOf(value) {
  var foundIndex = -1;
  this.each(function(e, i) {
    if (e === value) {
      foundIndex = i;
      return false;
    }
  });
  return foundIndex;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.initial"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>initial (count)](#apidoc.element.lazy.js.Sequence.prototype.initial)
- description and source-code
```javascript
function initial(count) {
  return new InitialSequence(this, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.inject"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>inject (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.inject)
- description and source-code
```javascript
function foldl(aggregator, memo) {
  return this.reduce(aggregator, memo);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.intersection"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>intersection (var_args)](#apidoc.element.lazy.js.Sequence.prototype.intersection)
- description and source-code
```javascript
function intersection(var_args) {
  if (arguments.length === 1 && isArray(arguments[0])) {
    return new SimpleIntersectionSequence(this, (/** @type {Array} */ var_args));
  } else {
    return new IntersectionSequence(this, arraySlice.call(arguments, 0));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.invoke"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>invoke (methodName)](#apidoc.element.lazy.js.Sequence.prototype.invoke)
- description and source-code
```javascript
function invoke(methodName) {
  return this.map(function(e) {
    return e[methodName]();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.isAsync"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.Sequence.prototype.isAsync)
- description and source-code
```javascript
function isAsync() {
  return this.parent ? this.parent.isAsync() : false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>isEmpty ()](#apidoc.element.lazy.js.Sequence.prototype.isEmpty)
- description and source-code
```javascript
function isEmpty() {
  return !this.any();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.join"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>join (delimiter)](#apidoc.element.lazy.js.Sequence.prototype.join)
- description and source-code
```javascript
function join(delimiter) {
  delimiter = typeof delimiter === "undefined" ? "," : String(delimiter);

  return this.reduce(function(str, e, i) {
    if (i > 0) {
      str += delimiter;
    }
    return str + e;
  }, "");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.last"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>last (count)](#apidoc.element.lazy.js.Sequence.prototype.last)
- description and source-code
```javascript
function last(count) {
  if (typeof count === "undefined") {
    return this.reverse().first();
  }
  return this.reverse().take(count).reverse();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>lastIndexOf (value)](#apidoc.element.lazy.js.Sequence.prototype.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(value) {
  var reversed = this.getIndex().reverse(),
      index    = reversed.indexOf(value);
  if (index !== -1) {
    index = reversed.length() - index - 1;
  }
  return index;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.map"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>map (mapFn)](#apidoc.element.lazy.js.Sequence.prototype.map)
- description and source-code
```javascript
function map(mapFn) {
  return new MappedSequence(this, createCallback(mapFn));
}
```
- example usage
```shell
...

The sequence-based paradigm of Lazy.js lets you do some pretty cool things that simply aren't possible with Underscore's array-based
 approach. One of these is the generation of **indefinite sequences**, which can go on forever, yet still support all of Lazy's
built-in mapping and filtering capabilities.

Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
  .map(function(e) { return Math.floor(e * 1000) + 1; })
  .uniq()
  .take(300)
  .each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.max"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>max (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.max)
- description and source-code
```javascript
function max(valueFn) {
  if (typeof valueFn !== "undefined") {
    return this.maxBy(valueFn);
  }

  return this.reduce(function(prev, current, i) {
    if (typeof prev === "undefined") {
      return current;
    }
    return current > prev ? current : prev;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.maxBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>maxBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.maxBy)
- description and source-code
```javascript
function maxBy(valueFn) {
  valueFn = createCallback(valueFn);
  return this.reduce(function(x, y) { return valueFn(y) > valueFn(x) ? y : x; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.memoize"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>memoize ()](#apidoc.element.lazy.js.Sequence.prototype.memoize)
- description and source-code
```javascript
function memoize() {
  return new MemoizedSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.min"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>min (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.min)
- description and source-code
```javascript
function min(valueFn) {
  if (typeof valueFn !== "undefined") {
    return this.minBy(valueFn);
  }

  return this.reduce(function(prev, current, i) {
    if (typeof prev === "undefined") {
      return current;
    }
    return current < prev ? current : prev;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.minBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>minBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.minBy)
- description and source-code
```javascript
function minBy(valueFn) {
  valueFn = createCallback(valueFn);
  return this.reduce(function(x, y) { return valueFn(y) < valueFn(x) ? y : x; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.none"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>none (predicate)](#apidoc.element.lazy.js.Sequence.prototype.none)
- description and source-code
```javascript
function none(predicate) {
  return !this.any(predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.ofType"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>ofType (type)](#apidoc.element.lazy.js.Sequence.prototype.ofType)
- description and source-code
```javascript
function ofType(type) {
  return this.filter(function(e) { return typeof e === type; });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.pipe"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>pipe (destination)](#apidoc.element.lazy.js.Sequence.prototype.pipe)
- description and source-code
```javascript
function pipe(destination) {
  this.toStream().pipe(destination);
}
```
- example usage
```shell
...

if (typeof Stream.Readable !== "undefined") {
Lazy.Sequence.prototype.toStream = function toStream(options) {
  return new LazyStream(this, options);
};

Lazy.Sequence.prototype.pipe = function pipe(destination) {
  this.toStream().pipe(destination);
};

function LazyStream(sequence, options) {
  options = Lazy(options || {})
    .extend({ objectMode: true })
    .toObject();
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.pluck"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>pluck (property)](#apidoc.element.lazy.js.Sequence.prototype.pluck)
- description and source-code
```javascript
function pluck(property) {
  return this.map(property);
}
```
- example usage
```shell
...
var people = getBigArrayOfPeople();
'''

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.reduce"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reduce (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.reduce)
- description and source-code
```javascript
function reduce(aggregator, memo) {
  if (arguments.length < 2) {
    return this.tail().reduce(aggregator, this.head());
  }

  var eachResult = this.each(function(e, i) {
    memo = aggregator(memo, e, i);
  });

  // TODO: Think of a way more efficient solution to this problem.
  if (eachResult instanceof AsyncHandle) {
    return eachResult.then(function() { return memo; });
  }

  return memo;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.reduceRight"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reduceRight (aggregator, memo)](#apidoc.element.lazy.js.Sequence.prototype.reduceRight)
- description and source-code
```javascript
function reduceRight(aggregator, memo) {
  if (arguments.length < 2) {
    return this.initial(1).reduceRight(aggregator, this.last());
  }

  // This bothers me... but frankly, calling reverse().reduce() is potentially
  // going to eagerly evaluate the sequence anyway; so it's really not an issue.
  var indexed = this.getIndex(),
      i = indexed.length() - 1;
  return indexed.reverse().reduce(function(m, e) {
    return aggregator(m, e, i--);
  }, memo);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.reject"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reject (rejectFn)](#apidoc.element.lazy.js.Sequence.prototype.reject)
- description and source-code
```javascript
function reject(rejectFn) {
  rejectFn = createCallback(rejectFn);
  return this.filter(function(e) { return !rejectFn(e); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.rest"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>rest (count)](#apidoc.element.lazy.js.Sequence.prototype.rest)
- description and source-code
```javascript
function rest(count) {
  return new DropSequence(this, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.reverse"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.Sequence.prototype.reverse)
- description and source-code
```javascript
function reverse() {
  return new ReversedSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.root"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>root ()](#apidoc.element.lazy.js.Sequence.prototype.root)
- description and source-code
```javascript
function root() {
  return this.parent.root();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.select"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>select (filterFn)](#apidoc.element.lazy.js.Sequence.prototype.select)
- description and source-code
```javascript
function select(filterFn) {
  return this.filter(filterFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.shuffle"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>shuffle ()](#apidoc.element.lazy.js.Sequence.prototype.shuffle)
- description and source-code
```javascript
function shuffle() {
  return new ShuffledSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.size"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>size ()](#apidoc.element.lazy.js.Sequence.prototype.size)
- description and source-code
```javascript
function size() {
  return this.getIndex().length();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.skip"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>skip (count)](#apidoc.element.lazy.js.Sequence.prototype.skip)
- description and source-code
```javascript
function drop(count) {
  return this.rest(count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.skipWhile"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>skipWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.skipWhile)
- description and source-code
```javascript
function skipWhile(predicate) {
  return this.dropWhile(predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.some"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>some (predicate)](#apidoc.element.lazy.js.Sequence.prototype.some)
- description and source-code
```javascript
function some(predicate) {
  predicate = createCallback(predicate, true);

  var success = false;
  this.each(function(e) {
    if (predicate(e)) {
      success = true;
      return false;
    }
  });
  return success;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.sort"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sort (sortFn, descending)](#apidoc.element.lazy.js.Sequence.prototype.sort)
- description and source-code
```javascript
function sort(sortFn, descending) {
  sortFn || (sortFn = compare);
  if (descending) { sortFn = reverseArguments(sortFn); }
  return new SortedSequence(this, sortFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.sortBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sortBy (sortFn, descending)](#apidoc.element.lazy.js.Sequence.prototype.sortBy)
- description and source-code
```javascript
function sortBy(sortFn, descending) {
  sortFn = createComparator(sortFn);
  if (descending) { sortFn = reverseArguments(sortFn); }
  return new SortedSequence(this, sortFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.sortedIndex"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sortedIndex (value)](#apidoc.element.lazy.js.Sequence.prototype.sortedIndex)
- description and source-code
```javascript
function sortedIndex(value) {
  var indexed = this.getIndex(),
      lower   = 0,
      upper   = indexed.length(),
      i;

  while (lower < upper) {
    i = (lower + upper) >>> 1;
    if (compare(indexed.get(i), value) === -1) {
      lower = i + 1;
    } else {
      upper = i;
    }
  }
  return lower;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.sum"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sum (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.sum)
- description and source-code
```javascript
function sum(valueFn) {
  if (typeof valueFn !== "undefined") {
    return this.sumBy(valueFn);
  }

  return this.reduce(function(x, y) { return x + y; }, 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.sumBy"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>sumBy (valueFn)](#apidoc.element.lazy.js.Sequence.prototype.sumBy)
- description and source-code
```javascript
function sumBy(valueFn) {
  valueFn = createCallback(valueFn);
  return this.reduce(function(x, y) { return x + valueFn(y); }, 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.tail"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>tail (count)](#apidoc.element.lazy.js.Sequence.prototype.tail)
- description and source-code
```javascript
function drop(count) {
  return this.rest(count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.take"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>take (count)](#apidoc.element.lazy.js.Sequence.prototype.take)
- description and source-code
```javascript
take = function (count) {
  return this.first(count);
}
```
- example usage
```shell
...

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
- 'filter(...)': iterates over the new array, creating yet *another* (potentially giant) array
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.takeWhile"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>takeWhile (predicate)](#apidoc.element.lazy.js.Sequence.prototype.takeWhile)
- description and source-code
```javascript
function takeWhile(predicate) {
  return new TakeWhileSequence(this, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.tap"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>tap (callback)](#apidoc.element.lazy.js.Sequence.prototype.tap)
- description and source-code
```javascript
function tap(callback) {
  return new TappedSequence(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.toArray"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toArray ()](#apidoc.element.lazy.js.Sequence.prototype.toArray)
- description and source-code
```javascript
function toArray() {
  return this.reduce(function(arr, element) {
    arr.push(element);
    return arr;
  }, []);
}
```
- example usage
```shell
...
    x = y;
    y += prev;
    return prev;
  };
}());

// Output: [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
fibonacci.take(10).toArray();
'''

OK, what else?

### Asynchronous iteration

You've probably [seen code snippets before](https://gist.github.com/dtao/2351944) that show how to iterate over an array asynchronously
 in JavaScript. But have you seen an example with functional goodness like this?
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.toObject"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toObject ()](#apidoc.element.lazy.js.Sequence.prototype.toObject)
- description and source-code
```javascript
function toObject() {
  return this.reduce(function(object, pair) {
    object[pair[0]] = pair[1];
    return object;
  }, {});
}
```
- example usage
```shell
...
  Lazy.Sequence.prototype.pipe = function pipe(destination) {
this.toStream().pipe(destination);
  };

  function LazyStream(sequence, options) {
options = Lazy(options || {})
  .extend({ objectMode: true })
  .toObject();

Stream.Readable.call(this, options);

this.sequence = sequence;
this.started  = false;

// Find delimiter on a (parent) sequence object if set
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.toStream"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toStream (options)](#apidoc.element.lazy.js.Sequence.prototype.toStream)
- description and source-code
```javascript
function toStream(options) {
  return new LazyStream(this, options);
}
```
- example usage
```shell
...

if (typeof Stream.Readable !== "undefined") {
Lazy.Sequence.prototype.toStream = function toStream(options) {
  return new LazyStream(this, options);
};

Lazy.Sequence.prototype.pipe = function pipe(destination) {
  this.toStream().pipe(destination);
};

function LazyStream(sequence, options) {
  options = Lazy(options || {})
    .extend({ objectMode: true })
    .toObject();
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.toString"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>toString (delimiter)](#apidoc.element.lazy.js.Sequence.prototype.toString)
- description and source-code
```javascript
function toString(delimiter) {
  return this.join(delimiter);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.union"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>union (var_args)](#apidoc.element.lazy.js.Sequence.prototype.union)
- description and source-code
```javascript
function union(var_args) {
  return this.concat(var_args).uniq();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.uniq"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>uniq (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.uniq)
- description and source-code
```javascript
function uniq(keyFn) {
  return new UniqueSequence(this, keyFn);
}
```
- example usage
```shell
...
The sequence-based paradigm of Lazy.js lets you do some pretty cool things that simply aren't possible with Underscore's array-based
 approach. One of these is the generation of **indefinite sequences**, which can go on forever, yet still support all of Lazy's
built-in mapping and filtering capabilities.

Here's an example. Let's say we want 300 unique random numbers between 1 and 1000.

'''javascript
Lazy.generate(Math.random)
  .map(function(e) { return Math.floor(e * 1000) + 1; })
  .uniq()
  .take(300)
  .each(function(e) { console.log(e); });
'''

Here's a slightly more advanced example: let's use Lazy.js to make a [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number
).

'''javascript
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.unique"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>unique (keyFn)](#apidoc.element.lazy.js.Sequence.prototype.unique)
- description and source-code
```javascript
function unique(keyFn) {
  return this.uniq(keyFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.value"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>value ()](#apidoc.element.lazy.js.Sequence.prototype.value)
- description and source-code
```javascript
function value() {
  return this.toArray();
}
```
- example usage
```shell
...
Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
- 'filter(...)': iterates over the new array, creating yet *another* (potentially giant) array
- 'take(5)': all that just for 5 elements!
...
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.where"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>where (properties)](#apidoc.element.lazy.js.Sequence.prototype.where)
- description and source-code
```javascript
function where(properties) {
  return this.filter(properties);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.without"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>without (var_args)](#apidoc.element.lazy.js.Sequence.prototype.without)
- description and source-code
```javascript
function without(var_args) {
  return new WithoutSequence(this, arraySlice.call(arguments, 0));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.Sequence.prototype.zip"></a>[function <span class="apidocSignatureSpan">lazy.js.Sequence.prototype.</span>zip (var_args)](#apidoc.element.lazy.js.Sequence.prototype.zip)
- description and source-code
```javascript
function zip(var_args) {
  if (arguments.length === 1) {
    return new SimpleZippedSequence(this, (/** @type {Array} */ var_args));
  } else {
    return new ZippedSequence(this, arraySlice.call(arguments, 0));
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.StreamLikeSequence"></a>[module lazy.js.StreamLikeSequence](#apidoc.module.lazy.js.StreamLikeSequence)

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.StreamLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>StreamLikeSequence ()](#apidoc.element.lazy.js.StreamLikeSequence.StreamLikeSequence)
- description and source-code
```javascript
function StreamLikeSequence() {}
```
- example usage
```shell
...
/**
 * @constructor
 */
function StreamedSequence(stream) {
  this.stream = stream;
}

StreamedSequence.prototype = new Lazy.StreamLikeSequence();

StreamedSequence.prototype.openStream = function(callback) {
  this.stream.resume();
  callback(this.stream);
};

/**
...
```



# <a name="apidoc.module.lazy.js.StreamLikeSequence.prototype"></a>[module lazy.js.StreamLikeSequence.prototype](#apidoc.module.lazy.js.StreamLikeSequence.prototype)

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.cancelCallback"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>cancelCallback (immediate)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.cancelCallback)
- description and source-code
```javascript
cancelCallback = function (immediate) {
  if (!immediate) return;

  immediate._onImmediate = null;

  immediateQueue.remove(immediate);

  if (!immediateQueue.head) {
    process._needImmediateCallback = false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.isAsync"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>isAsync ()](#apidoc.element.lazy.js.StreamLikeSequence.prototype.isAsync)
- description and source-code
```javascript
function isAsync() {
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.lines"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>lines ()](#apidoc.element.lazy.js.StreamLikeSequence.prototype.lines)
- description and source-code
```javascript
function lines() {
  return this.split("\n");
}
```
- example usage
```shell
...
'''

For convenience, specialized helper methods for dealing with either file streams or HTTP streams are also offered. (**Note: this
 API will probably change.**)

'''javascript
// Read the first 5 lines from a file:
Lazy.readFile("path/to/file")
.lines()
.take(5)
.each(doSomething);

// Read lines 5-10 from an HTTP response.
Lazy.makeHttpRequest("http://example.com")
.lines()
.drop(5)
...
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.match"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>match (pattern)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.match)
- description and source-code
```javascript
function match(pattern) {
  return new MatchedStreamSequence(this, pattern);
}
```
- example usage
```shell
...
'''

This way we can read the first five lines of an arbitrarily large string (without pre-populating a huge array) and map/reduce on
 it just as with any other sequence.

Similarly with 'String.match': let's say we wanted to find the first 5 alphanumeric matches in a string. With Lazy.js, it's easy
!

'''javascript
var firstFiveWords = Lazy(text).match(/[a-z0-9]+/i).take(5);
'''

Piece of cake.

### Stream processing

Lazy.js can wrap *streams* in Node.js as well.
...
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.onNextCallback"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>onNextCallback (callback, arg1, arg2, arg3)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.onNextCallback)
- description and source-code
```javascript
onNextCallback = function (callback, arg1, arg2, arg3) {
  if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  var i, args;

  switch (arguments.length) {
    // fast cases
    case 1:
      break;
    case 2:
      args = [arg1];
      break;
    case 3:
      args = [arg1, arg2];
      break;
    default:
      args = [arg1, arg2, arg3];
      for (i = 4; i < arguments.length; i++)
        // extend array dynamically, makes .apply run much faster in v6.0.0
        args[i - 1] = arguments[i];
      break;
  }
  return createImmediate(args, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StreamLikeSequence.prototype.split"></a>[function <span class="apidocSignatureSpan">lazy.js.StreamLikeSequence.prototype.</span>split (delimiter)](#apidoc.element.lazy.js.StreamLikeSequence.prototype.split)
- description and source-code
```javascript
function split(delimiter) {
  return new SplitStreamSequence(this, delimiter);
}
```
- example usage
```shell
...
### String processing

Now here's something you may not have even thought of: 'String.match' and 'String.split'. In JavaScript, each of these methods returns
 an *array* of substrings. If you think about it, this often means doing more work than necessary; but it's the quickest way (from
 a developer's standpoint) to get the job done.

For example, suppose you wanted the first five lines of a block of text. You could always do this:

'''javascript
var firstFiveLines = text.split("\n").slice(0, 5);
'''

But of course, this actually splits *the entire string* into every single line. If the string is very large, this is quite wasteful
.

With Lazy.js, we don't need to split up an entire string just to treat it as a sequence of lines. We can get the same effect by
wrapping the string with 'Lazy' and calling 'split':

'''javascript
...
```



# <a name="apidoc.module.lazy.js.StringLikeSequence"></a>[module lazy.js.StringLikeSequence](#apidoc.module.lazy.js.StringLikeSequence)

#### <a name="apidoc.element.lazy.js.StringLikeSequence.StringLikeSequence"></a>[function <span class="apidocSignatureSpan">lazy.js.</span>StringLikeSequence ()](#apidoc.element.lazy.js.StringLikeSequence.StringLikeSequence)
- description and source-code
```javascript
function StringLikeSequence() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.define"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.</span>define (methodName, overrides)](#apidoc.element.lazy.js.StringLikeSequence.define)
- description and source-code
```javascript
function define(methodName, overrides) {
  if (!overrides || typeof overrides.get !== 'function') {
    throw new Error("A custom string-like sequence must implement *at least* get!");
  }

  return defineSequenceType(StringLikeSequence, methodName, overrides);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.StringLikeSequence.prototype"></a>[module lazy.js.StringLikeSequence.prototype](#apidoc.module.lazy.js.StringLikeSequence.prototype)

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.charAt"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>charAt (i)](#apidoc.element.lazy.js.StringLikeSequence.prototype.charAt)
- description and source-code
```javascript
function charAt(i) {
  return this.get(i);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.charCodeAt"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>charCodeAt (i)](#apidoc.element.lazy.js.StringLikeSequence.prototype.charCodeAt)
- description and source-code
```javascript
function charCodeAt(i) {
  var char = this.charAt(i);
  if (!char) { return NaN; }

  return char.charCodeAt(0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.contains"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>contains (substring)](#apidoc.element.lazy.js.StringLikeSequence.prototype.contains)
- description and source-code
```javascript
function contains(substring) {
  return this.indexOf(substring) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.drop"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>drop (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.drop)
- description and source-code
```javascript
function drop(count) {
  return this.substring(count);
}
```
- example usage
```shell
...
  .lines()
  .take(5)
  .each(doSomething);

// Read lines 5-10 from an HTTP response.
Lazy.makeHttpRequest("http://example.com")
  .lines()
  .drop(5)
  .take(5)
  .each(doSomething);
'''

In each case, the elements in the sequence will be "chunks" of data most likely comprising multiple lines. The 'lines()' method
splits each chunk into lines (lazily, of course).

***
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.endsWith"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>endsWith (suffix)](#apidoc.element.lazy.js.StringLikeSequence.prototype.endsWith)
- description and source-code
```javascript
function endsWith(suffix) {
  return this.substring(this.length() - suffix.length).toString() === suffix;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.first"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>first (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.first)
- description and source-code
```javascript
function first(count) {
  if (typeof count === "undefined") {
    return this.charAt(0);
  }

  return this.substring(0, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.getIterator"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>getIterator ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.getIterator)
- description and source-code
```javascript
function getIterator() {
  return new CharIterator(this);
}
```
- example usage
```shell
...

  if (typeof Lazy === 'undefined' && typeof require === 'function') {
Lazy = require('../lazy.js');
  }

  if (typeof Symbol !== 'undefined') {
Lazy.Sequence.prototype[Symbol.iterator] = function() {
  return new IteratorAdapter(this.getIterator());
}

function IteratorAdapter(iterator) {
  this.iterator = iterator;
}

IteratorAdapter.prototype.next = function next() {
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>indexOf (substring, startIndex)](#apidoc.element.lazy.js.StringLikeSequence.prototype.indexOf)
- description and source-code
```javascript
function indexOf(substring, startIndex) {
  return this.toString().indexOf(substring, startIndex);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.last"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>last (count)](#apidoc.element.lazy.js.StringLikeSequence.prototype.last)
- description and source-code
```javascript
function last(count) {
  if (typeof count === "undefined") {
    return this.charAt(this.length() - 1);
  }

  return this.substring(this.length() - count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>lastIndexOf (substring, startIndex)](#apidoc.element.lazy.js.StringLikeSequence.prototype.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(substring, startIndex) {
  return this.toString().lastIndexOf(substring, startIndex);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.mapString"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>mapString (mapFn)](#apidoc.element.lazy.js.StringLikeSequence.prototype.mapString)
- description and source-code
```javascript
function mapString(mapFn) {
  return new MappedStringLikeSequence(this, mapFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.match"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>match (pattern)](#apidoc.element.lazy.js.StringLikeSequence.prototype.match)
- description and source-code
```javascript
function match(pattern) {
  return new StringMatchSequence(this, pattern);
}
```
- example usage
```shell
...
'''

This way we can read the first five lines of an arbitrarily large string (without pre-populating a huge array) and map/reduce on
 it just as with any other sequence.

Similarly with 'String.match': let's say we wanted to find the first 5 alphanumeric matches in a string. With Lazy.js, it's easy
!

'''javascript
var firstFiveWords = Lazy(text).match(/[a-z0-9]+/i).take(5);
'''

Piece of cake.

### Stream processing

Lazy.js can wrap *streams* in Node.js as well.
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.reverse"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>reverse ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.reverse)
- description and source-code
```javascript
function reverse() {
  return new ReversedStringLikeSequence(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.split"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>split (delimiter)](#apidoc.element.lazy.js.StringLikeSequence.prototype.split)
- description and source-code
```javascript
function split(delimiter) {
  return new SplitStringSequence(this, delimiter);
}
```
- example usage
```shell
...
### String processing

Now here's something you may not have even thought of: 'String.match' and 'String.split'. In JavaScript, each of these methods returns
 an *array* of substrings. If you think about it, this often means doing more work than necessary; but it's the quickest way (from
 a developer's standpoint) to get the job done.

For example, suppose you wanted the first five lines of a block of text. You could always do this:

'''javascript
var firstFiveLines = text.split("\n").slice(0, 5);
'''

But of course, this actually splits *the entire string* into every single line. If the string is very large, this is quite wasteful
.

With Lazy.js, we don't need to split up an entire string just to treat it as a sequence of lines. We can get the same effect by
wrapping the string with 'Lazy' and calling 'split':

'''javascript
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.startsWith"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>startsWith (prefix)](#apidoc.element.lazy.js.StringLikeSequence.prototype.startsWith)
- description and source-code
```javascript
function startsWith(prefix) {
  return this.substring(0, prefix.length).toString() === prefix;
}
```
- example usage
```shell
...
'''

Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
...
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.substring"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>substring (start, stop)](#apidoc.element.lazy.js.StringLikeSequence.prototype.substring)
- description and source-code
```javascript
function substring(start, stop) {
  return new StringSegment(this, start, stop);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.toLowerCase"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toLowerCase ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toLowerCase)
- description and source-code
```javascript
function toLowerCase() {
  return this.mapString(function(char) { return char.toLowerCase(); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.toString"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toString ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.join("");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.toUpperCase"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>toUpperCase ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.toUpperCase)
- description and source-code
```javascript
function toUpperCase() {
  return this.mapString(function(char) { return char.toUpperCase(); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.StringLikeSequence.prototype.value"></a>[function <span class="apidocSignatureSpan">lazy.js.StringLikeSequence.prototype.</span>value ()](#apidoc.element.lazy.js.StringLikeSequence.prototype.value)
- description and source-code
```javascript
function value() {
  return this.toString();
}
```
- example usage
```shell
...
Suppose we're using this array to back some sort of search-as-you-type functionality, where users can search for people by their
 last names. Naturally we want to put some reasonable constraints on our problem space, so we'll provide up to 5 results at a time
. Supposing the user types "Smith", we could therefore fetch results using something like this (using Underscore):

'''javascript
var results = _.chain(people)
  .pluck('lastName')
  .filter(function(name) { return name.startsWith('Smith'); })
  .take(5)
  .value();
'''

This query does a lot of stuff:

- 'pluck('lastName')': iterates over the array and creates a new (potentially giant) array
- 'filter(...)': iterates over the new array, creating yet *another* (potentially giant) array
- 'take(5)': all that just for 5 elements!
...
```



# <a name="apidoc.module.lazy.js.extensions"></a>[module lazy.js.extensions](#apidoc.module.lazy.js.extensions)

#### <a name="apidoc.element.lazy.js.extensions.0"></a>[function <span class="apidocSignatureSpan">lazy.js.extensions.</span>0 (source)](#apidoc.element.lazy.js.extensions.0)
- description and source-code
```javascript
0 = function (source) {
  if (isES6Generator(source)) {
    return new GeneratorWrapper(source);

  } else if (isES6Map(source)) {
    return new MapWrapper(source);

  } else if (isES6Set(source) || isES6Iterator(source)) {
    return new IterableWrapper(source);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lazy.js.extensions.1"></a>[function <span class="apidocSignatureSpan">lazy.js.extensions.</span>1 (source)](#apidoc.element.lazy.js.extensions.1)
- description and source-code
```javascript
1 = function (source) {
  if (source instanceof Stream) {
    return new StreamedSequence(source);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lazy.js.util"></a>[module lazy.js.util](#apidoc.module.lazy.js.util)

#### <a name="apidoc.element.lazy.js.util.isHarmonySupported"></a>[function <span class="apidocSignatureSpan">lazy.js.util.</span>isHarmonySupported ()](#apidoc.element.lazy.js.util.isHarmonySupported)
- description and source-code
```javascript
function isHarmonySupported() {
  var version = process.version.split('.');

  // We'll only bother checking Node versions 0.10 and greater
  if (version[0] == 'v0' && Number(version[1]) < 10) {
    return false;
  }

  try {
    eval('(function*() {})');
    return true;
  } catch (e) {
    return false;
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
