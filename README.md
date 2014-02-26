# iostreams-bootstrap

Bootstrap stream provider for [iostreams](https://github.com/webcast-io/iostreams)

[![Build Status](https://travis-ci.org/webcast-io/iostreams-bootstrap.png)](https://travis-ci.org/webcast-io/iostreams-bootstrap?branch=master)
[![Coverage Status](https://coveralls.io/repos/webcast-io/iostreams-bootstrap/badge.png?branch=master)](https://coveralls.io/r/webcast-io/iostreams-bootstrap?branch=master)
[![Dependency Status](https://david-dm.org/webcast-io/iostreams-bootstrap.png?theme=shields.io)](https://david-dm.org/webcast-io/iostreams-bootstrap)

## Install

    $ npm install iostreams iostreams-bootstrap

## Usage

```js
var iostreams = require('iostreams');

iostreams.use(require('iostreams-bootstrap'));

// Getting an input stream
iostreams.getInputStream('bootstrap://home/ben/lolcat.png', function(err, inputStream) {

});

// Getting an output stream
iostreams.getOutputStream('bootstrap://home/ben/lolcat.png', function(err, outputStream) {

});

// Getting an input and output stream
iostrams.getInputAndOutputStream(
  'bootstrap://inputpath',
  'bootstrap://outputpath',
  function(err, inputStream, outputStream) {
    intputStream.pipe(outputStream);
  }
);
```

## Licence

MIT