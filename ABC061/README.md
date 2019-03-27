### ABC061
[問題ページ](https://atcoder.jp/contests/abc061/tasks)

### A-Between Two Integers
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    const C = parseInt(arg.split("\n")[0].split(" ")[2]);
    console.log(A <= C && C <= B ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Counting Roads
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    const M = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    const path = arg.split("\n").slice(1, M + 1);
    const map = new Array(N).fill(0);
    path.forEach(v => {
        let a = parseInt(v.split(' ')[0]) - 1;
        let b = parseInt(v.split(' ')[1]) - 1;
        map[a]++;
        map[b]++;
    })
    map.forEach(v => console.log(v));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```