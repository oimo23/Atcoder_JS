### ABC018
[問題ページ](https://atcoder.jp/contests/abc018/tasks)

### A-豆まき
```JavaScript
"use strict";
    
const main = arg => {
    const scores = arg.trim().split("\n").map(n=>~~n);
    const sorted = [...scores].sort((a,b)=>b-a);

    for(let i in scores) {
        console.log(sorted.indexOf(scores[i]) + 1);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-文字列の反転
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    let S  = arg[0].split("");
    const N  = ~~arg[1];
    const lr = arg.slice(2, N + 2).map(n=>n.split(" "));
    
    for(let i=0; i<N; i++) {
        let reversed = S.slice(lr[i][0] - 1, lr[i][1]).reverse().join("");
        
        S.splice(lr[i][0] - 1, lr[i][1] - lr[i][0] + 1, reversed);
        S = S.join("").split("");
    }
    
    console.log(S.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```