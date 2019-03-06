### ABC098
[問題ページ](https://atcoder.jp/contests/abc098/tasks)

### A-Add Sub Mul
```JavaScript
"use strict";

function main(arg) {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    const calc = [];
    
    calc.push(A + B);
    calc.push(A - B);
    calc.push(A * B);
    
    console.log(parseInt(Math.max(...calc)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Cut and Count
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    const S = arg.split("\n")[1].split("");
    const scores = [];
    const letter = new Set(S);
    
    for(let i=1 ; i<N ; i++) {
        let cnt   = 0;
        let left  = S.slice(0, i);
        let right = S.slice(i, N);
        
        letter.forEach(value=> {
           if(left.indexOf(value) !== -1 && right.indexOf(value) !== -1 ) {
               cnt++;
           }
        });
        
        scores.push(cnt);
    }
    
    console.log(Math.max(...scores));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```