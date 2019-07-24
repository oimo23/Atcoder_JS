### ABC050
[問題ページ](https://atcoder.jp/contests/abc050/tasks)

### A-Addition and Subtraction Easy
```JavaScript
"use strict";
    
const main = arg => {
    const formula = arg.split("\n")[0].split(" ");
    const A   = parseInt(formula[0]);
    const ope = formula[1];
    const B   = parseInt(formula[2]);
    
    console.log(ope == "+" ? A + B : A - B);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Contest with Drinks Easy
```JavaScript
"use strict";

const main = arg => {
    arg = arg.trim().split("\n")
    const N = parseInt(arg[0]);
    const T = arg[1].split(" ").map(n=>~~n);
    const M = parseInt(arg[2]);
    const drinks = arg.slice(3, M + 3).map(n=>n.split(" ").map(l=>parseInt(l)));
    
    const baseTime = T.reduce((m,n)=>m+n);
    
    for(let i in drinks) {
        console.log((baseTime - T[drinks[i][0] - 1]) + drinks[i][1]);
    }
}

main(require('fs').readFileSync('/dev/stdin', 'utf-8'))

```