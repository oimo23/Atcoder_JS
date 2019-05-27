### ABC009
[問題ページ](https://atcoder.jp/contests/abc009/tasks)

### A-引越し作業
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0];
    
    console.log(Math.ceil(N / 2));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-心配性な富豪、ファミリーレストランに行く。
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0];
    const A = arg.slice(1, N + 1).map(n=>~~n).sort((a,b)=>b-a);
    const setA = new Set(A);
    
    console.log([...setA][1]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```