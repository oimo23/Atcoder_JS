### ABC058
[問題ページ](https://atcoder.jp/contests/abc058/tasks)

### A-ι⊥l
```JavaScript
"use strict";
    
const main = arg => {
    const a = arg.split("\n")[0].split(" ")[0];
    const b = arg.split("\n")[0].split(" ")[1];
    const c = arg.split("\n")[0].split(" ")[2];
    
    console.log(b - a == c - b ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-∵∴∵
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = arg[0].split("");
    const B = arg[1].split("");
    
    const length = A.length;
    let answer   = [];
    
    for(let i=0; i<length; i++) {
        answer.push(A[i]);
        
        if(B[i]) {
            answer.push(B[i]);
        }
    }
    
    console.log(answer.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```