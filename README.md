# api documentation for  [entities (v1.1.1)](https://github.com/fb55/node-entities)  [![npm package](https://img.shields.io/npm/v/npmdoc-entities.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-entities) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-entities.svg)](https://travis-ci.org/npmdoc/node-npmdoc-entities)
#### Encode & decode XML/HTML entities with ease

[![NPM](https://nodei.co/npm/entities.png?downloads=true)](https://www.npmjs.com/package/entities)

[![apidoc](https://npmdoc.github.io/node-npmdoc-entities/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-entities_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-entities/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-entities/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-entities/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Felix Boehm",
        "email": "me@feedic.com"
    },
    "bugs": {
        "url": "https://github.com/fb55/node-entities/issues"
    },
    "dependencies": {},
    "description": "Encode & decode XML/HTML entities with ease",
    "devDependencies": {
        "coveralls": "*",
        "istanbul": "*",
        "jshint": "2",
        "mocha": "1",
        "mocha-lcov-reporter": "*"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "6e5c2d0a5621b5dadaecef80b90edfb5cd7772f0",
        "tarball": "https://registry.npmjs.org/entities/-/entities-1.1.1.tgz"
    },
    "homepage": "https://github.com/fb55/node-entities",
    "jshintConfig": {
        "eqeqeq": true,
        "freeze": true,
        "latedef": "nofunc",
        "noarg": true,
        "nonbsp": true,
        "quotmark": "double",
        "undef": true,
        "unused": true,
        "trailing": true,
        "eqnull": true,
        "proto": true,
        "smarttabs": true,
        "node": true,
        "globals": {
            "describe": true,
            "it": true
        }
    },
    "keywords": [
        "html",
        "xml",
        "entity",
        "encoding"
    ],
    "license": "BSD-like",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "feedic",
            "email": "me@feedic.com"
        }
    ],
    "name": "entities",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/fb55/node-entities.git"
    },
    "scripts": {
        "coveralls": "npm run lint && npm run lcov && (cat coverage/lcov.info | coveralls || exit 0)",
        "lcov": "istanbul cover _mocha --report lcovonly -- -R spec",
        "lint": "jshint index.js lib/*.js test/*.js",
        "test": "mocha && npm run lint"
    },
    "version": "1.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module entities](#apidoc.module.entities)
1.  [function <span class="apidocSignatureSpan">entities.</span>decode (data, level)](#apidoc.element.entities.decode)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTML (str)](#apidoc.element.entities.decodeHTML)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTML4 (str)](#apidoc.element.entities.decodeHTML4)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTML4Strict (str)](#apidoc.element.entities.decodeHTML4Strict)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTML5 (str)](#apidoc.element.entities.decodeHTML5)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTML5Strict (str)](#apidoc.element.entities.decodeHTML5Strict)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeHTMLStrict (str)](#apidoc.element.entities.decodeHTMLStrict)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeStrict (data, level)](#apidoc.element.entities.decodeStrict)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeXML (str)](#apidoc.element.entities.decodeXML)
1.  [function <span class="apidocSignatureSpan">entities.</span>decodeXMLStrict (str)](#apidoc.element.entities.decodeXMLStrict)
1.  [function <span class="apidocSignatureSpan">entities.</span>encode (data, level)](#apidoc.element.entities.encode)
1.  [function <span class="apidocSignatureSpan">entities.</span>encodeHTML (data)](#apidoc.element.entities.encodeHTML)
1.  [function <span class="apidocSignatureSpan">entities.</span>encodeHTML4 (data)](#apidoc.element.entities.encodeHTML4)
1.  [function <span class="apidocSignatureSpan">entities.</span>encodeHTML5 (data)](#apidoc.element.entities.encodeHTML5)
1.  [function <span class="apidocSignatureSpan">entities.</span>encodeXML (data)](#apidoc.element.entities.encodeXML)
1.  [function <span class="apidocSignatureSpan">entities.</span>escape (data)](#apidoc.element.entities.escape)

#### [module entities.decode](#apidoc.module.entities.decode)
1.  [function <span class="apidocSignatureSpan">entities.decode.</span>HTML (str)](#apidoc.element.entities.decode.HTML)
1.  [function <span class="apidocSignatureSpan">entities.decode.</span>HTMLStrict (str)](#apidoc.element.entities.decode.HTMLStrict)
1.  [function <span class="apidocSignatureSpan">entities.decode.</span>XML (str)](#apidoc.element.entities.decode.XML)

#### [module entities.encode](#apidoc.module.entities.encode)
1.  [function <span class="apidocSignatureSpan">entities.encode.</span>HTML (data)](#apidoc.element.entities.encode.HTML)
1.  [function <span class="apidocSignatureSpan">entities.encode.</span>XML (data)](#apidoc.element.entities.encode.XML)
1.  [function <span class="apidocSignatureSpan">entities.encode.</span>escape (data)](#apidoc.element.entities.encode.escape)



# <a name="apidoc.module.entities"></a>[module entities](#apidoc.module.entities)

#### <a name="apidoc.element.entities.decode"></a>[function <span class="apidocSignatureSpan">entities.</span>decode (data, level)](#apidoc.element.entities.decode)
- description and source-code
```javascript
decode = function (data, level){
	return (!level || level <= 0 ? decode.XML : decode.HTML)(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeHTML"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTML (str)](#apidoc.element.entities.decodeHTML)
- description and source-code
```javascript
decodeHTML = function (str){
		return String(str).replace(re, replacer);
	}
```
- example usage
```shell
...
'''javascript
var entities = require("entities");
//encoding
entities.encodeXML("&#38;");  // "&amp;#38;"
entities.encodeHTML("&#38;"); // "&amp;&num;38&semi;"
//decoding
entities.decodeXML("asdf &amp; &#xFF; &#xFC; &apos;");  // "asdf & ÿ ü '"
entities.decodeHTML("asdf &amp; &yuml; &uuml; &apos;"); // "asdf & ÿ ü '"
'''

<!-- TODO extend API -->

---

License: BSD-like
...
```

#### <a name="apidoc.element.entities.decodeHTML4"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTML4 (str)](#apidoc.element.entities.decodeHTML4)
- description and source-code
```javascript
decodeHTML4 = function (str){
		return String(str).replace(re, replacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeHTML4Strict"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTML4Strict (str)](#apidoc.element.entities.decodeHTML4Strict)
- description and source-code
```javascript
decodeHTML4Strict = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeHTML5"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTML5 (str)](#apidoc.element.entities.decodeHTML5)
- description and source-code
```javascript
decodeHTML5 = function (str){
		return String(str).replace(re, replacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeHTML5Strict"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTML5Strict (str)](#apidoc.element.entities.decodeHTML5Strict)
- description and source-code
```javascript
decodeHTML5Strict = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeHTMLStrict"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeHTMLStrict (str)](#apidoc.element.entities.decodeHTMLStrict)
- description and source-code
```javascript
decodeHTMLStrict = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeStrict"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeStrict (data, level)](#apidoc.element.entities.decodeStrict)
- description and source-code
```javascript
decodeStrict = function (data, level){
	return (!level || level <= 0 ? decode.XML : decode.HTMLStrict)(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decodeXML"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeXML (str)](#apidoc.element.entities.decodeXML)
- description and source-code
```javascript
decodeXML = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
...

'''javascript
var entities = require("entities");
//encoding
entities.encodeXML("&#38;");  // "&amp;#38;"
entities.encodeHTML("&#38;"); // "&amp;&num;38&semi;"
//decoding
entities.decodeXML("asdf &amp; &#xFF; &#xFC; &apos;");  // "asdf & ÿ ü '"
entities.decodeHTML("asdf &amp; &yuml; &uuml; &apos;"); // "asdf & ÿ ü '"
'''

<!-- TODO extend API -->

---
...
```

#### <a name="apidoc.element.entities.decodeXMLStrict"></a>[function <span class="apidocSignatureSpan">entities.</span>decodeXMLStrict (str)](#apidoc.element.entities.decodeXMLStrict)
- description and source-code
```javascript
decodeXMLStrict = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encode"></a>[function <span class="apidocSignatureSpan">entities.</span>encode (data, level)](#apidoc.element.entities.encode)
- description and source-code
```javascript
encode = function (data, level){
	return (!level || level <= 0 ? encode.XML : encode.HTML)(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encodeHTML"></a>[function <span class="apidocSignatureSpan">entities.</span>encodeHTML (data)](#apidoc.element.entities.encodeHTML)
- description and source-code
```javascript
encodeHTML = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
...

###…use 'entities'

'''javascript
var entities = require("entities");
//encoding
entities.encodeXML("&#38;");  // "&amp;#38;"
entities.encodeHTML("&#38;"); // "&amp;&num;38&semi;"
//decoding
entities.decodeXML("asdf &amp; &#xFF; &#xFC; &apos;");  // "asdf & ÿ ü '"
entities.decodeHTML("asdf &amp; &yuml; &uuml; &apos;"); // "asdf & ÿ ü '"
'''

<!-- TODO extend API -->
...
```

#### <a name="apidoc.element.entities.encodeHTML4"></a>[function <span class="apidocSignatureSpan">entities.</span>encodeHTML4 (data)](#apidoc.element.entities.encodeHTML4)
- description and source-code
```javascript
encodeHTML4 = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encodeHTML5"></a>[function <span class="apidocSignatureSpan">entities.</span>encodeHTML5 (data)](#apidoc.element.entities.encodeHTML5)
- description and source-code
```javascript
encodeHTML5 = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encodeXML"></a>[function <span class="apidocSignatureSpan">entities.</span>encodeXML (data)](#apidoc.element.entities.encodeXML)
- description and source-code
```javascript
encodeXML = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
...
    npm i entities

###…use 'entities'

'''javascript
var entities = require("entities");
//encoding
entities.encodeXML("&#38;");  // "&amp;#38;"
entities.encodeHTML("&#38;"); // "&amp;&num;38&semi;"
//decoding
entities.decodeXML("asdf &amp; &#xFF; &#xFC; &apos;");  // "asdf & ÿ ü '"
entities.decodeHTML("asdf &amp; &yuml; &uuml; &apos;"); // "asdf & ÿ ü '"
'''

<!-- TODO extend API -->
...
```

#### <a name="apidoc.element.entities.escape"></a>[function <span class="apidocSignatureSpan">entities.</span>escape (data)](#apidoc.element.entities.escape)
- description and source-code
```javascript
function escapeXML(data){
	return data
			.replace(re_xmlChars, singleCharReplacer)
			.replace(re_astralSymbols, astralReplacer)
			.replace(re_nonASCII, singleCharReplacer);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.entities.decode"></a>[module entities.decode](#apidoc.module.entities.decode)

#### <a name="apidoc.element.entities.decode.HTML"></a>[function <span class="apidocSignatureSpan">entities.decode.</span>HTML (str)](#apidoc.element.entities.decode.HTML)
- description and source-code
```javascript
HTML = function (str){
		return String(str).replace(re, replacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decode.HTMLStrict"></a>[function <span class="apidocSignatureSpan">entities.decode.</span>HTMLStrict (str)](#apidoc.element.entities.decode.HTMLStrict)
- description and source-code
```javascript
HTMLStrict = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.decode.XML"></a>[function <span class="apidocSignatureSpan">entities.decode.</span>XML (str)](#apidoc.element.entities.decode.XML)
- description and source-code
```javascript
XML = function (str){
		return String(str).replace(re, replace);
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.entities.encode"></a>[module entities.encode](#apidoc.module.entities.encode)

#### <a name="apidoc.element.entities.encode.HTML"></a>[function <span class="apidocSignatureSpan">entities.encode.</span>HTML (data)](#apidoc.element.entities.encode.HTML)
- description and source-code
```javascript
HTML = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encode.XML"></a>[function <span class="apidocSignatureSpan">entities.encode.</span>XML (data)](#apidoc.element.entities.encode.XML)
- description and source-code
```javascript
XML = function (data){
		return data
				.replace(re, func)
				.replace(re_astralSymbols, astralReplacer)
				.replace(re_nonASCII, singleCharReplacer);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.entities.encode.escape"></a>[function <span class="apidocSignatureSpan">entities.encode.</span>escape (data)](#apidoc.element.entities.encode.escape)
- description and source-code
```javascript
function escapeXML(data){
	return data
			.replace(re_xmlChars, singleCharReplacer)
			.replace(re_astralSymbols, astralReplacer)
			.replace(re_nonASCII, singleCharReplacer);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
