# iostreams-file

File stream provider for [iostreams](https://github.com/webcast-io/iostreams)

## Install

    $ npm install iostreams iostreams-file

## Usage

    var iostreams = require('iostreams');

    iostreams.use(require('iostreams-file'));

    // Getting an input stream
    iostreams.getInputStream('file://home/ben/lolcat.png', function(err, inputStream) {

    });

    // Getting an output stream
    iostreams.getOutputStream('file://home/ben/lolcat.png', function(err, outputStream) {

    });

    // Getting an input and output stream
    iostrams.getInputAndOutputStream(
      'file://inputpath',
      'file://outputpath',
      function(err, inputStream, outputStream) {
        intputStream.pipe(outputStream);
      }
    );

## Licence

MIT