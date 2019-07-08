### ABC100
[問題ページ](https://atcoder.jp/contests/abc100/tasks)

### A-Happy Birthday!
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    if(A <=8 && B <=8) {
        console.log("Yay!");
    } else {
        console.log(":(");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Ringo's Favorite Numbers
```JavaScript
"use strict";
 
const main = arg => {
    arg = arg.split("\n")[0].split(" ");
    const D = arg[0];
    const N = arg[1] == "100" ? "101" : arg[1];
    let zeros = [];
    
    if(parseInt(N) === 0) {
        console.log(0);
        return;
    }
    
    for(let i=0; i<D; i++) {
        zeros.push("00");
    }
    
    console.log(N + zeros.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```