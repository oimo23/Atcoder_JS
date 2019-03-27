### ABC065
[問題ページ](https://atcoder.jp/contests/abc065/tasks)

### A-Expired?
```JavaScript
"use strict";

const main = arg => {
    const X = parseInt(arg.split("\n")[0].split(" ")[0]);
    const A = parseInt(arg.split("\n")[0].split(" ")[1]);
    const B = parseInt(arg.split("\n")[0].split(" ")[2]);
    
    if((B - A) >= X + 1) {
        console.log("dangerous");
    } else if((B - A) <= X && (B - A) > 0) {
        console.log("safe");
    } else {
        console.log("delicious");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```