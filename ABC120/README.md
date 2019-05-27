### ABC120
[問題ページ](https://atcoder.jp/contests/abc120/tasks)

### A-Favorite Sound
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    const C = parseInt(arg.split("\n")[0].split(" ")[2]);
    console.log(Math.floor(B / A) >= C ? C : Math.floor(B / A));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-K-th Common Divisor
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    const K = parseInt(arg.split("\n")[0].split(" ")[2]);
    const list = [];
    
    for(let i=1; i<=Math.min(A,B); i++) {
        if(A % i == 0 && B % i == 0) {
            list.push(i);
        }
    }
    
    console.log(list[list.length - K]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Unification
```JavaScript
"use strict";

const main = arg => {
    let N = arg.split("\n")[0].split("");  
    const red = N.filter(n=>n=="0").length;
    const blue = N.length - red;
 
    console.log(Math.min(red, blue) * 2);   
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```