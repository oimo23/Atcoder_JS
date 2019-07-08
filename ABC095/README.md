### ABC095
[問題ページ](https://atcoder.jp/contests/abc095/tasks)

### A-Something on It
```JavaScript
"use strict";

const main = arg => {
    const toppings = arg.split("\n")[0].split("");
    console.log(700 + (100 * toppings.filter(n=>n=="o").length));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Bitter Alchemy
```JavaScript
"use strict";

const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    let   X = arg.split("\n")[0].split(" ")[1];
    const m = arg.split("\n").slice(1, N + 1).map(n=>parseInt(n));
    
    X = (X - m.reduce((m,n)=>m+n));
    
    console.log(Math.floor(X / Math.min(...m)) + N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```