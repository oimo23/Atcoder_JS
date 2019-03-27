### ABC063
[問題ページ](https://atcoder.jp/contests/abc063/tasks)

### A-Restricted
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).reduce((m,n)=>m+n);
    console.log(N < 10 ? N : "error" );
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Varied
```JavaScript
"use strict";

const main = arg => {
    const S   = arg.split("\n")[0].split("");
    const set = new Set(S);
    
    console.log(S.length == set.size ? "yes" : "no");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```