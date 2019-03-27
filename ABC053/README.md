### ABC053
[問題ページ](https://atcoder.jp/contests/abc053/tasks)

### A-ABC/ARC
```JavaScript
"use strict";
    
const main = arg => {
    let X = parseInt(arg.split("\n")[0].split(" ")[0]);
    
    console.log(X >= 1200 ? "ARC" : "ABC");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```