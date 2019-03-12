### ABC086
[問題ページ](https://atcoder.jp/contests/abc086/tasks)

### A-Product
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    console.log((A * B) % 2 === 0 ? "Even" : "Odd");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-1 21
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    
    const N = parseInt(A + B);
    for(let i=1; i<N; i++) {
        if(Math.pow(i, 2) === N) {
            console.log("Yes");
            return;
        } 
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```