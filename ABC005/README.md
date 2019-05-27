### ABC005
[問題ページ](https://atcoder.jp/contests/abc005/tasks)

### A-AtCoder Crackers
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const x = arg[0].split(" ")[0];
    const y = arg[0].split(" ")[1];
    
    console.log(Math.floor(y / x));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Cakes and Donuts
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0];
    const T = arg.slice(1, N + 1).map(n=>~~n);
    
    console.log(Math.min(...T));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```