# fs-tail
[![Build Status](https://travis-ci.org/classdojo/fs-tail.svg?branch=master)](https://travis-ci.org/classdojo/fs-tail)
[![codecov.io](https://codecov.io/github/classdojo/fs-tail/coverage.svg?branch=master)](https://codecov.io/github/classdojo/fs-tail?branch=master)
[![NPM version](https://badge.fury.io/js/fs-tail.png)](http://badge.fury.io/js/fs-tail)

```tail -f``` functionality for node.js using pull streams.  Significantly faster than delegating to the operating system with ```child_processes.exec```.   

```javascript
var FsTail = require("fs-tail");

// Available options - defaults are shown.
var options = {
  start: 0 //Start on byte 0 of file.
  EOFAfter: 500 //emit EOF after 500ms of no data.
};

var tail = FsTail("./someFile.txt", options);
tail.on("EOF", function() {
  console.log("Reached end of file");
});
tail.pipe(anotherStream);
```
