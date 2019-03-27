### ABC073
[問題ページ](https://atcoder.jp/contests/abc073/tasks)

### A-September 9
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    console.log(N.split("").filter(n=>n==9).length ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Theater
```JavaScript
"use strict";
    
const main = arg => {
    const N  = arg.split("\n")[0];
    const lr = arg.split("\n").slice(1, N + 1);
    let answer = 0;
    
    for(let i=0; i<N; i++) {
        answer += lr[i].split(" ")[1] - lr[i].split(" ")[0] + 1;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```