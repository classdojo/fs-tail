# fs-tail
[![Build Status](https://travis-ci.org/classdojo/fs-tail.svg?branch=master)](https://travis-ci.org/classdojo/fs-tail)
[![codecov.io](https://codecov.io/github/classdojo/fs-tail/coverage.svg?branch=master)](https://codecov.io/github/classdojo/fs-tail?branch=master)
[![NPM version](https://badge.fury.io/js/fs-tail.png)](http://badge.fury.io/js/fs-tail)


```javascript
var FsTail = require("fs-tail");

var tail = FsTail("./someFile.txt");
tail.on("EOF", function() {
  console.log("Reached end of file");
});
tail.pipe(someStream);
```