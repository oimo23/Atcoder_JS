### ABC015
[問題ページ](https://atcoder.jp/contests/abc015/tasks)

### A-高橋くんの研修
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S1 = arg[0];
    const S2 = arg[1];
    
    console.log(S1.length > S2.length ? S1 : S2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-高橋くんの集計
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0];
    const bugs = arg[1].split(" ").map(n=>~~n);
    
    console.log(Math.ceil(bugs.reduce((m,n)=>m+n) / (N - bugs.filter(n=>n===0).length)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```