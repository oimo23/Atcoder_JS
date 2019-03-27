### ABC054
[問題ページ](https://atcoder.jp/contests/abc054/tasks)

### A-One Card Poker
```JavaScript
"use strict";
    
const main = arg => {
    let A = parseInt(arg.split("\n")[0].split(" ")[0]);
    let B = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if(A == 1) A = 14;
    if(B == 1) B = 14;
    
    if(A == B) {
        console.log("Draw");
    } else if(A > B) {
        console.log("Alice")
    } else {
        console.log("Bob")
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```