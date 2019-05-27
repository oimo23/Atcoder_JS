### ABC033
[問題ページ](https://atcoder.jp/contests/abc033/tasks)

### A-暗証番号
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split("");
    const set = new Set(N);

    console.log(set.size === 1 ? "SAME" : "DIFFERENT");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-町の合併
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0];
    const towns = arg.slice(1, N + 1);
    
    const sum = towns.map(n=>n.split(" ")[1]).reduce((m,n)=>~~m + ~~n);
    
    for(let i in towns) {
        if(towns[i].split(" ")[1] > sum / 2) {
            console.log(towns[i].split(" ")[0]);
            return;
        }
    }
    
    console.log("atcoder");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-数式の書き換え
```JavaScript
"use strict";

const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("+");
    let cnt = 0;
    
    for(let i in S) {
        const multi = S[i].split("*").reduce((m,n)=>m*n);
        
        if(parseInt(multi) !== 0) {
            cnt++;
        }
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```