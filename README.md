# suitcss-preprocessor

Preprocessor for working with SUIT CSS packages.

[![Build Status](https://travis-ci.org/suitcss/preprocessor.png)](http://travis-ci.org/suitcss/preprocessor)

## Installation

```
npm install suitcss-preprocessor
```

## Usage

```
suitcss input.css output.css
```

## Features

Provides a CLI and Node.js interface for a preprocessor that combines
[rework-suit](https://github.com/suitcss/rework-suit) with
[autoprefixer](https://github.com/ai/autoprefixer).

## API

#### Command Line

```
Usage: suitcss [<input>] [<output>]

Options:

  -h, --help     output usage information
  -V, --version  output the version number
  -w, --watch    watch the input file for changes
  -v, --verbose  log verbose output for debugging

Examples:

  # pass an input and output file:
  $ suitcss input.css output.css

  # watch the input file for changes:
  $ suitcss --watch input.css output.css

  # unix-style piping to stdin and stdout:
  $ cat input.css | suitcss | grep background-color
```

#### Node.js

```js
var suitcss = require('suitcss');
var fs = require('fs');

var css = fs.readFileSync('index.css', 'utf8');
var converted = myth(css);

fs.writeFileSync('converted.css', converted);
```

## Acknowledgements

Based on [Myth](https://github.com/segmentio/myth) by Segment.io.