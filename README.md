# npmdoc-csv-parse

#### basic api documentation for  [csv-parse (v1.2.0)](http://csv.adaltas.com/parse/)  [![npm package](https://img.shields.io/npm/v/npmdoc-csv-parse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-csv-parse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-csv-parse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-csv-parse)

#### CSV parsing implementing the Node.js `stream.Transform` API

[![NPM](https://nodei.co/npm/csv-parse.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/csv-parse)

- [https://npmdoc.github.io/node-npmdoc-csv-parse/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-csv-parse/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-csv-parse/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "contributors": [
        {
            "name": "David Worms",
            "url": "http://www.adaltas.com"
        },
        {
            "name": "Will White",
            "url": "https://github.com/willwhite"
        },
        {
            "name": "Justin Latimer",
            "url": "https://github.com/justinlatimer"
        },
        {
            "name": "jonseymour",
            "url": "https://github.com/jonseymour"
        },
        {
            "name": "pascalopitz",
            "url": "https://github.com/pascalopitz"
        },
        {
            "name": "Josh Pschorr",
            "url": "https://github.com/jpschorr"
        },
        {
            "name": "Elad Ben-Israel",
            "url": "https://github.com/eladb"
        },
        {
            "name": "Philippe Plantier",
            "url": "https://github.com/phipla"
        },
        {
            "name": "Tim Oxley",
            "url": "https://github.com/timoxley"
        },
        {
            "name": "Damon Oehlman",
            "url": "https://github.com/DamonOehlman"
        },
        {
            "name": "Alexandru Topliceanu",
            "url": "https://github.com/topliceanu"
        },
        {
            "name": "Visup",
            "url": "https://github.com/visup"
        },
        {
            "name": "Edmund von der Burg",
            "url": "https://github.com/evdb"
        },
        {
            "name": "Douglas Christopher Wilson",
            "url": "https://github.com/dougwilson"
        },
        {
            "name": "Joe Eaves",
            "url": "https://github.com/Joeasaurus"
        },
        {
            "name": "Mark Stosberg",
            "url": "https://github.com/markstos"
        }
    ],
    "dependencies": {},
    "description": "CSV parsing implementing the Node.js 'stream.Transform' API",
    "devDependencies": {
        "coffee-script": "1.10.0",
        "csv-generate": "1.0.0",
        "csv-spectrum": "1.0.0",
        "each": "0.6.1",
        "mocha": "2.5.3",
        "should": "9.0.2"
    },
    "directories": {},
    "dist": {
        "shasum": "047b73868ab9a85746e885f637f9ed0fb645a425",
        "tarball": "https://registry.npmjs.org/csv-parse/-/csv-parse-1.2.0.tgz"
    },
    "gitHead": "2ec704e757000eb0ecb17dc231a9a669b66c702e",
    "homepage": "http://csv.adaltas.com/parse/",
    "keywords": [
        "csv",
        "parse",
        "parser"
    ],
    "license": "BSD-3-Clause",
    "main": "./lib",
    "maintainers": [
        {
            "name": "david"
        }
    ],
    "name": "csv-parse",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "http://www.github.com/wdavidw/node-csv-parse"
    },
    "scripts": {
        "coffee": "coffee -b -o lib src",
        "pretest": "coffee -b -o lib src",
        "test": "NODE_ENV=test ./node_modules/.bin/mocha --compilers coffee:coffee-script/register --reporter dot"
    },
    "version": "1.2.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
