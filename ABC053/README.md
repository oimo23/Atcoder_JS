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

### B-A to Z String
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S = arg[0].split("");
    
    let flag    = false;
    let answer  = [];
    let counter = 0;
    
    const start = S.indexOf("A");
    const end   = S.reverse().indexOf("Z");
    
    console.log((S.length - end) - start);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```