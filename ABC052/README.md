### ABC052
[問題ページ](https://atcoder.jp/contests/abc052/tasks)

### A-Two Rectangles
```JavaScript
"use strict";
    
const main = arg => {
    const rectangles = arg.split("\n")[0].split(" ");
    const A = rectangles[0] * rectangles[1];
    const B = rectangles[2] * rectangles[3];
    console.log(Math.max(A, B));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));
w
```