### ABC046
[問題ページ](https://atcoder.jp/contests/abc046/tasks)

### A-AtCoDeerくんとペンキ
```JavaScript
"use strict";
    
const main = arg => {
    const colors = arg.split("\n")[0].split(" ");
    const set = new Set(colors);
    
    console.log(set.size);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AtCoDeerくんとボール色塗り / Painting Balls with AtCoDeer
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const K = ~~arg[0].split(" ")[1];
    
    console.log(K * (Math.pow((K-1), N-1)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```