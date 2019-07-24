### ABC094
[問題ページ](https://atcoder.jp/contests/abc094/tasks)

### A-Cats and Dogs
```JavaScript
"use strict";

const main = arg => {
    arg = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const A = arg[0];
    const B = arg[1];
    const X = arg[2];
    
    console.log(A <= X && B >= Math.abs(A-X) ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Toll Gates
```JavaScript
"use strict";

const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    const M = parseInt(arg.split("\n")[0].split(" ")[1]);
    const X = parseInt(arg.split("\n")[0].split(" ")[2]);
    const m = arg.split("\n")[1].split(" ").map(n=>parseInt(n));
    
    let rightCost = 0;
    let leftCost  = 0;
    
    for(let i=X; i<=N; i++) {
        if(m.indexOf(i) != -1) rightCost++;
    }
    
    for(let i=X; i>0; i--) {
        if(m.indexOf(i) != -1) leftCost++;
    }
    
    console.log(Math.min(rightCost, leftCost));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Many Medians
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const X = arg[1].split(" ").map(n=>parseInt(n));
    const sortedX = [...X].sort((a,b)=>a-b);
    
    const medianOne = sortedX[(N / 2) - 1];
    const medianTwo = sortedX[N / 2];

    let answer = [];
    
    for(let i in X) {
        if(X[i] < medianTwo) {
            answer.push(medianTwo);
        } else {
            answer.push(medianOne);
        }
    }
    
    console.log(answer.join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```