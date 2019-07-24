### ABC044
[問題ページ](https://atcoder.jp/contests/abc044/tasks)

### A-高橋君とホテルイージー
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    const K = arg.split("\n")[1];
    const X = arg.split("\n")[2];
    const Y = arg.split("\n")[3];
    
    console.log(N - K > 0 ? (X * K) + Y * (N - K) : X * N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-美しい文字列 / Beautiful Strings
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const w = arg[0].split("");
    
    const set = new Set(w);
    const unique = [...set];
    
    for(let i in unique) {
        if(w.filter(n=>n===unique[i]).length % 2 !== 0) {
            console.log("No");
            return;
        }   
    }
    
    console.log("Yes");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```