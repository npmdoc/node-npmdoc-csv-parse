# api documentation for  [csv-parse (v1.2.0)](http://csv.adaltas.com/parse/)  [![npm package](https://img.shields.io/npm/v/npmdoc-csv-parse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-csv-parse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-csv-parse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-csv-parse)
#### CSV parsing implementing the Node.js `stream.Transform` API

[![NPM](https://nodei.co/npm/csv-parse.png?downloads=true)](https://www.npmjs.com/package/csv-parse)

[![apidoc](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-csv-parse_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-csv-parse/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-csv-parse/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "contributors": [
        {
            "name": "David Worms",
            "email": "david@adaltas.com",
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
            "name": "david",
            "email": "david@adaltas.com"
        }
    ],
    "name": "csv-parse",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "http://www.github.com/wdavidw/node-csv-parse"
    },
    "scripts": {
        "coffee": "coffee -b -o lib src",
        "pretest": "coffee -b -o lib src",
        "test": "NODE_ENV=test ./node_modules/.bin/mocha --compilers coffee:coffee-script/register --reporter dot"
    },
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module csv-parse](#apidoc.module.csv-parse)
1.  [function <span class="apidocSignatureSpan">csv-parse.</span>Parser (options)](#apidoc.element.csv-parse.Parser)
1.  object <span class="apidocSignatureSpan">csv-parse.</span>Parser.prototype

#### [module csv-parse.Parser](#apidoc.module.csv-parse.Parser)
1.  [function <span class="apidocSignatureSpan">csv-parse.</span>Parser (options)](#apidoc.element.csv-parse.Parser.Parser)
1.  [function <span class="apidocSignatureSpan">csv-parse.Parser.</span>super_ (options)](#apidoc.element.csv-parse.Parser.super_)

#### [module csv-parse.Parser.prototype](#apidoc.module.csv-parse.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>__push (line)](#apidoc.element.csv-parse.Parser.prototype.__push)
1.  [function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>__write (chars, end)](#apidoc.element.csv-parse.Parser.prototype.__write)
1.  [function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>_flush (callback)](#apidoc.element.csv-parse.Parser.prototype._flush)
1.  [function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>_transform (chunk, encoding, callback)](#apidoc.element.csv-parse.Parser.prototype._transform)



# <a name="apidoc.module.csv-parse"></a>[module csv-parse](#apidoc.module.csv-parse)

#### <a name="apidoc.element.csv-parse.Parser"></a>[function <span class="apidocSignatureSpan">csv-parse.</span>Parser (options)](#apidoc.element.csv-parse.Parser)
- description and source-code
```javascript
Parser = function (options) {
  var base, base1, base10, base11, base12, base13, base14, base15, base16, base2, base3, base4, base5, base6, base7, base8, base9
, k, v;
  if (options == null) {
    options = {};
  }
  options.objectMode = true;
  this.options = {};
  for (k in options) {
    v = options[k];
    this.options[k] = v;
  }
  stream.Transform.call(this, this.options);
  if ((base = this.options).rowDelimiter == null) {
    base.rowDelimiter = null;
  }
  if (typeof this.options.rowDelimiter === 'string') {
    this.options.rowDelimiter = [this.options.rowDelimiter];
  }
  if ((base1 = this.options).delimiter == null) {
    base1.delimiter = ',';
  }
  if ((base2 = this.options).quote == null) {
    base2.quote = '"';
  }
  if ((base3 = this.options).escape == null) {
    base3.escape = '"';
  }
  if ((base4 = this.options).columns == null) {
    base4.columns = null;
  }
  if ((base5 = this.options).comment == null) {
    base5.comment = '';
  }
  if ((base6 = this.options).objname == null) {
    base6.objname = false;
  }
  if ((base7 = this.options).trim == null) {
    base7.trim = false;
  }
  if ((base8 = this.options).ltrim == null) {
    base8.ltrim = false;
  }
  if ((base9 = this.options).rtrim == null) {
    base9.rtrim = false;
  }
  if ((base10 = this.options).auto_parse == null) {
    base10.auto_parse = false;
  }
  if ((base11 = this.options).auto_parse_date == null) {
    base11.auto_parse_date = false;
  }
  if ((base12 = this.options).relax == null) {
    base12.relax = false;
  }
  if ((base13 = this.options).relax_column_count == null) {
    base13.relax_column_count = false;
  }
  if ((base14 = this.options).skip_empty_lines == null) {
    base14.skip_empty_lines = false;
  }
  if ((base15 = this.options).max_limit_on_data_read == null) {
    base15.max_limit_on_data_read = 128000;
  }
  if ((base16 = this.options).skip_lines_with_empty_values == null) {
    base16.skip_lines_with_empty_values = false;
  }
  this.lines = 0;
  this.count = 0;
  this.skipped_line_count = 0;
  this.empty_line_count = 0;
  this.is_int = /^(\-|\+)?([1-9]+[0-9]*)$/;
  this.is_float = function(value) {
    return (value - parseFloat(value) + 1) >= 0;
  };
  this._ = {};
  this._.decoder = new StringDecoder();
  this._.quoting = false;
  this._.commenting = false;
  this._.field = null;
  this._.nextChar = null;
  this._.closingQuote = 0;
  this._.line = [];
  this._.chunks = [];
  this._.rawBuf = '';
  this._.buf = '';
  if (this.options.rowDelimiter) {
    this._.rowDelimiterLength = Math.max.apply(Math, this.options.rowDelimiter.map(function(v) {
      return v.length;
    }));
  }
  return this;
}
```
- example usage
```shell
...
  options = {};
}
records = options.objname ? {} : [];
if (data instanceof Buffer) {
  decoder = new StringDecoder();
  data = decoder.write(data);
}
parser = new parse.Parser(options);
parser.push = function(record) {
  if (options.objname) {
    return records[record[0]] = record[1];
  } else {
    return records.push(record);
  }
};
...
```



# <a name="apidoc.module.csv-parse.Parser"></a>[module csv-parse.Parser](#apidoc.module.csv-parse.Parser)

#### <a name="apidoc.element.csv-parse.Parser.Parser"></a>[function <span class="apidocSignatureSpan">csv-parse.</span>Parser (options)](#apidoc.element.csv-parse.Parser.Parser)
- description and source-code
```javascript
Parser = function (options) {
  var base, base1, base10, base11, base12, base13, base14, base15, base16, base2, base3, base4, base5, base6, base7, base8, base9
, k, v;
  if (options == null) {
    options = {};
  }
  options.objectMode = true;
  this.options = {};
  for (k in options) {
    v = options[k];
    this.options[k] = v;
  }
  stream.Transform.call(this, this.options);
  if ((base = this.options).rowDelimiter == null) {
    base.rowDelimiter = null;
  }
  if (typeof this.options.rowDelimiter === 'string') {
    this.options.rowDelimiter = [this.options.rowDelimiter];
  }
  if ((base1 = this.options).delimiter == null) {
    base1.delimiter = ',';
  }
  if ((base2 = this.options).quote == null) {
    base2.quote = '"';
  }
  if ((base3 = this.options).escape == null) {
    base3.escape = '"';
  }
  if ((base4 = this.options).columns == null) {
    base4.columns = null;
  }
  if ((base5 = this.options).comment == null) {
    base5.comment = '';
  }
  if ((base6 = this.options).objname == null) {
    base6.objname = false;
  }
  if ((base7 = this.options).trim == null) {
    base7.trim = false;
  }
  if ((base8 = this.options).ltrim == null) {
    base8.ltrim = false;
  }
  if ((base9 = this.options).rtrim == null) {
    base9.rtrim = false;
  }
  if ((base10 = this.options).auto_parse == null) {
    base10.auto_parse = false;
  }
  if ((base11 = this.options).auto_parse_date == null) {
    base11.auto_parse_date = false;
  }
  if ((base12 = this.options).relax == null) {
    base12.relax = false;
  }
  if ((base13 = this.options).relax_column_count == null) {
    base13.relax_column_count = false;
  }
  if ((base14 = this.options).skip_empty_lines == null) {
    base14.skip_empty_lines = false;
  }
  if ((base15 = this.options).max_limit_on_data_read == null) {
    base15.max_limit_on_data_read = 128000;
  }
  if ((base16 = this.options).skip_lines_with_empty_values == null) {
    base16.skip_lines_with_empty_values = false;
  }
  this.lines = 0;
  this.count = 0;
  this.skipped_line_count = 0;
  this.empty_line_count = 0;
  this.is_int = /^(\-|\+)?([1-9]+[0-9]*)$/;
  this.is_float = function(value) {
    return (value - parseFloat(value) + 1) >= 0;
  };
  this._ = {};
  this._.decoder = new StringDecoder();
  this._.quoting = false;
  this._.commenting = false;
  this._.field = null;
  this._.nextChar = null;
  this._.closingQuote = 0;
  this._.line = [];
  this._.chunks = [];
  this._.rawBuf = '';
  this._.buf = '';
  if (this.options.rowDelimiter) {
    this._.rowDelimiterLength = Math.max.apply(Math, this.options.rowDelimiter.map(function(v) {
      return v.length;
    }));
  }
  return this;
}
```
- example usage
```shell
...
  options = {};
}
records = options.objname ? {} : [];
if (data instanceof Buffer) {
  decoder = new StringDecoder();
  data = decoder.write(data);
}
parser = new parse.Parser(options);
parser.push = function(record) {
  if (options.objname) {
    return records[record[0]] = record[1];
  } else {
    return records.push(record);
  }
};
...
```

#### <a name="apidoc.element.csv-parse.Parser.super_"></a>[function <span class="apidocSignatureSpan">csv-parse.Parser.</span>super_ (options)](#apidoc.element.csv-parse.Parser.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform))
    return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function')
      this._transform = options.transform;

    if (typeof options.flush === 'function')
      this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function() {
    if (typeof this._flush === 'function')
      this._flush(function(er) {
        done(stream, er);
      });
    else
      done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.csv-parse.Parser.prototype"></a>[module csv-parse.Parser.prototype](#apidoc.module.csv-parse.Parser.prototype)

#### <a name="apidoc.element.csv-parse.Parser.prototype.__push"></a>[function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>__push (line)](#apidoc.element.csv-parse.Parser.prototype.__push)
- description and source-code
```javascript
__push = function (line) {
  var field, i, j, len, lineAsColumns, rawBuf, row;
  if (this.options.skip_lines_with_empty_values && line.join('').trim() === '') {
    return;
  }
  row = null;
  if (this.options.columns === true) {
    this.options.columns = line;
    rawBuf = '';
    return;
  } else if (typeof this.options.columns === 'function') {
    this.options.columns = this.options.columns(line);
    rawBuf = '';
    return;
  }
  if (!this._.line_length && line.length > 0) {
    this._.line_length = this.options.columns ? this.options.columns.length : line.length;
  }
  if (line.length === 1 && line[0] === '') {
    this.empty_line_count++;
  } else if (line.length !== this._.line_length) {
    if (this.options.relax_column_count) {
      this.skipped_line_count++;
    } else if (this.options.columns != null) {
      throw Error("Number of columns on line " + this.lines + " does not match header");
    } else {
      throw Error("Number of columns is inconsistent on line " + this.lines);
    }
  } else {
    this.count++;
  }
  if (this.options.columns != null) {
    lineAsColumns = {};
    for (i = j = 0, len = line.length; j < len; i = ++j) {
      field = line[i];
      if (this.options.columns[i] === false) {
        continue;
      }
      lineAsColumns[this.options.columns[i]] = field;
    }
    if (this.options.objname) {
      row = [lineAsColumns[this.options.objname], lineAsColumns];
    } else {
      row = lineAsColumns;
    }
  } else {
    row = line;
  }
  if (this.count < this.options.from) {
    return;
  }
  if (this.count > this.options.to) {
    return;
  }
  if (this.options.raw) {
    this.push({
      raw: this._.rawBuf,
      row: row
    });
    return this._.rawBuf = '';
  } else {
    return this.push(row);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csv-parse.Parser.prototype.__write"></a>[function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>__write (chars, end)](#apidoc.element.csv-parse.Parser.prototype.__write)
- description and source-code
```javascript
__write = function (chars, end) {
  var areNextCharsDelimiter, areNextCharsRowDelimiters, auto_parse, char, escapeIsQuote, i, isDelimiter, isEscape, isNextCharAComment
, isQuote, isRowDelimiter, isRowDelimiterLength, is_float, is_int, l, ltrim, nextCharPos, ref, ref1, ref2, ref3, ref4, remainingBuffer
, results, rowDelimiter, rtrim, wasCommenting;
  is_int = (function(_this) {
    return function(value) {
      if (typeof _this.is_int === 'function') {
        return _this.is_int(value);
      } else {
        return _this.is_int.test(value);
      }
    };
  })(this);
  is_float = (function(_this) {
    return function(value) {
      if (typeof _this.is_float === 'function') {
        return _this.is_float(value);
      } else {
        return _this.is_float.test(value);
      }
    };
  })(this);
  auto_parse = (function(_this) {
    return function(value) {
      var m;
      if (!_this.options.auto_parse) {
        return value;
      }
      if (is_int(value)) {
        value = parseInt(value);
      } else if (is_float(value)) {
        value = parseFloat(value);
      } else if (_this.options.auto_parse_date) {
        m = Date.parse(value);
        if (!isNaN(m)) {
          value = new Date(m);
        }
      }
      return value;
    };
  })(this);
  ltrim = this.options.trim || this.options.ltrim;
  rtrim = this.options.trim || this.options.rtrim;
  chars = this._.buf + chars;
  l = chars.length;
  i = 0;
  if (this.lines === 0 && 0xFEFF === chars.charCodeAt(0)) {
    i++;
  }
  while (i < l) {
    if (!end) {
      remainingBuffer = chars.substr(i, l - i);
      if ((!this.options.rowDelimiter && i + 3 > l) || (!this._.commenting && l - i < this.options.comment.length && this.options
.comment.substr(0, l - i) === remainingBuffer) || (this.options.rowDelimiter && l - i < this._.rowDelimiterLength && this.options
.rowDelimiter.some(function(rd) {
        return rd.substr(0, l - i) === remainingBuffer;
      })) || (this.options.rowDelimiter && this._.quoting && l - i < (this.options.quote.length + this._.rowDelimiterLength) &&
this.options.rowDelimiter.some((function(_this) {
        return function(rd) {
          return (_this.options.quote + rd).substr(0, l - i) === remainingBuffer;
        };
      })(this))) || (l - i <= this.options.delimiter.length && this.options.delimiter.substr(0, l - i) === remainingBuffer) || (
l - i <= this.options.escape.length && this.options.escape.substr(0, l - i) === remainingBuffer)) {
        break;
      }
    }
    char = this._.nextChar ? this._.nextChar : chars.charAt(i);
    this._.nextChar = l > i + 1 ? chars.charAt(i + 1) : '';
    if (this.options.raw) {
      this._.rawBuf += char;
    }
    if (this.options.rowDelimiter == null) {
      nextCharPos = i;
      rowDelimiter = null;
      if (!this._.quoting && (char === '\n' || char === '\r')) {
        rowDelimiter = char;
        nextCharPos += 1;
      } else if (!(!this._.quoting && char === this.options.quote) && (this._.nextChar === '\n' || this._.nextChar === '\r')) {
        rowDelimiter = this._.nextChar;
        nextCharPos += 2;
        if (this.raw) {
          rawBuf += this._.nextChar;
        }
      }
      if (rowDelimiter) {
        if (rowDelimiter === '\r' && chars.charAt(nextCharPos) === '\n') {
          rowDelimiter += '\n';
        }
        this.options.rowDelimiter = [rowDelimiter];
        this._.rowDelimiterLength = rowDelimiter.length;
      }
    }
    if (!this._.commenting && char === this.options.escape) {
      escapeIsQuote = this.options.escape === this.options.quote;
      isEscape = this._.nextChar === this.options.escape;
      isQuote = this._.nextChar === this.options.quote;
      if (!(escapeIsQuote && (this._.field == null) && !this._.quoting) && (isEscape || isQuote)) {
        i++;
        char = this._.nextChar;
        this._.nextChar = chars.charAt(i + 1);
        if (this._.field == null) {
          this._.field = '';
        }
        this._.field += char;
        if (this.options.raw) {
          this._.rawBuf += char;
        }
        i++;
        continue;
      }
    } ...
```
- example usage
```shell
...
  parser.push = function(record) {
    if (options.objname) {
      return records[record[0]] = record[1];
    } else {
      return records.push(record);
    }
  };
  parser.__write(data, false);
  if (data instanceof Buffer) {
    parser.__write(data.end(), true);
  }
  parser._flush((function() {}));
  return records;
};
...
```

#### <a name="apidoc.element.csv-parse.Parser.prototype._flush"></a>[function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>_flush (callback)](#apidoc.element.csv-parse.Parser.prototype._flush)
- description and source-code
```javascript
_flush = function (callback) {
  var err, error;
  try {
    this.__write(this._.decoder.end(), true);
    if (this._.quoting) {
      this.emit('error', new Error("Quoted field not terminated at line " + (this.lines + 1)));
      return;
    }
    if (this._.line.length > 0) {
      this.__push(this._.line);
    }
    return callback();
  } catch (error) {
    err = error;
    return this.emit('error', err);
  }
}
```
- example usage
```shell
...
      return records.push(record);
    }
  };
  parser.__write(data, false);
  if (data instanceof Buffer) {
    parser.__write(data.end(), true);
  }
  parser._flush((function() {}));
  return records;
};
...
```

#### <a name="apidoc.element.csv-parse.Parser.prototype._transform"></a>[function <span class="apidocSignatureSpan">csv-parse.Parser.prototype.</span>_transform (chunk, encoding, callback)](#apidoc.element.csv-parse.Parser.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, encoding, callback) {
  var err, error;
  if (chunk instanceof Buffer) {
    chunk = this._.decoder.write(chunk);
  }
  try {
    this.__write(chunk, false);
    return callback();
  } catch (error) {
    err = error;
    return this.emit('error', err);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
