# fs-tail

```javascript
var FsTail = require("fs-tail");

var tail = FsTail("./someFile.txt");
tail.on("EOF", function() {
  console.log("Reached end of file");
});
tail.pipe(someStream);
```