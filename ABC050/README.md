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