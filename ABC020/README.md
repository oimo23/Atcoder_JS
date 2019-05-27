### ABC020
[問題ページ](https://atcoder.jp/contests/abc020/tasks)

### A-クイズ
```JavaScript
"use strict";
    
const main = arg => {
    const Q = parseInt(arg.split("\n")[0]);
    console.log(Q === 1 ? "ABC" : "chokudai");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-足し算
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0].split(" ").join("");
    console.log(N * 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```