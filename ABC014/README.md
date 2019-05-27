### ABC014
[問題ページ](https://atcoder.jp/contests/abc014/tasks)

### A-けんしょう先生のお菓子配り
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const a = arg[0];
    const b = arg[1];
    
    console.log(a % b === 0 ? 0 : b - (a % b));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-価格の合計
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const X = parseInt(arg[0].split(" ")[1]).toString(2).split("").reverse();
    const a = arg[1].split(" ").map(n=>~~n);
    
    let answer = 0;
    
    for(let i=0; i<X.length; i++) {
        if(X[i] == 1) {
            answer += a[i];
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```