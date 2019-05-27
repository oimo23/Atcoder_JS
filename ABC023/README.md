### ABC023
[問題ページ](https://atcoder.jp/contests/abc023/tasks)

### A-加算王
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    console.log(N.split("").map(n=>parseInt(n)).reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-手芸王
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const procedure = arg[1].split("");
    
    const correct = [];
    
    for(let i=0; i<N / 2; i++) {
        if(i === 0) {
            correct.push("b");
        } else if(i % 3 === 1) {
            correct.unshift("a");
            correct.push("c");
        } else if(i % 3 === 2) {
            correct.unshift("c");
            correct.push("a");

        } else if(i % 3 === 0) {
            correct.unshift("b");
            correct.push("b");
        }
        
        if(correct.join("") === procedure.join("")) {
            console.log(i);
            return;
        }
    }
    
    console.log(-1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```