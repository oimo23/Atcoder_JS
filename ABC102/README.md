### ABC102
[問題ページ](https://atcoder.jp/contests/abc102/tasks)

### A-Multiple of 2 and N
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    console.log( N % 2 === 0 ? N : N * 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Maximum Difference
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[1].split(" ").sort((a,b)=>a-b);
    console.log(A[A.length-1] - A[0]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Linear Approximation
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const A = arg[1].split(" ").map(n=>parseInt(n));
    
    let list = [];
    
    for(let i in A) {
        let temp = A[i] - (parseInt(i) + 1);
        
        list.push(temp);
    }
    
    let b = list.sort((a,b)=>a-b)[Math.floor(N / 2)];
    
    let answer = 0;

    for(let i in A) {
        let temp = Math.abs(A[i] - ((parseInt(i) + 1) + b));
        
        answer += temp;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```