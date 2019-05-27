### ABC036
[問題ページ](https://atcoder.jp/contests/abc036/tasks)

### A-お茶
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    
    console.log(B % A === 0 ? B / A : Math.floor(B / A) + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-回転
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const table = arg.slice(1, N + 1).map(n=>n.split(""));
    
    let answer = [];
    
    for(let i=0; i<N; i++) {
        answer[i] = [];
        for(let j=0; j<N; j++) {
            answer[i].push(table[N - j - 1][i]);   
        }
        answer[i] = answer[i].join("");
    }
    
    console.log(answer.join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```