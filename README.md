# hashing_stream
`hashing_stream` is a simple pass thru stream which hashes incoming data.

## Installation

    npm install hashing-stream

## Usage
```js
var HashingStream = require('hashing_stream').HashingStream;

fs.createReadStream('fillerama.txt')
  .pipe(new HashingStream('sha1'))
  .on('end', function (hash) {
    hash.digest('hex'); // => '65f3bd7e5bed93ebef9fb5338d9b9a19deb5c2d5'
  });
```