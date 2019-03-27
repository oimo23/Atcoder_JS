### ABC067
[問題ページ](https://atcoder.jp/contests/abc067/tasks)

### A-Sharing Cookies
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if( A % 3 === 0 || B % 3 === 0 || (A + B) % 3 === 0 ) {
        console.log("Possible");
    } else {
        console.log("Impossible");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Snake Toy
```JavaScript
"use strict";

const main = arg => {
    const K = arg.split("\n")[0].split(" ")[1];
    const l = arg.split("\n")[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>b-a);
    
    console.log(l.slice(0, K).reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```