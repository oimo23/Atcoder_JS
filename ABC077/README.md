### ABC077
[問題ページ](https://atcoder.jp/contests/abc077/tasks)

### A-Rotation
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0];
    const B = arg.split("\n")[1];
    
    console.log(B.split("").reverse().join("") == A ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Around Square
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    
    if(N === 1 || N === 2) {
        console.log(1);
        return;
    }
    
    for(let i=1; i<N; i++) {
        if(Math.pow(i, 2) > N) {
            console.log(Math.pow(i-1, 2));
            return;
        }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```