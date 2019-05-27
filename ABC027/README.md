### ABC027
[問題ページ](https://atcoder.jp/contests/abc027/tasks)

### A-長方形
```JavaScript
"use strict";
    
const main = arg => {
    const l = arg.split("\n")[0].split(" ");
    
    for(let i in l) {
        if(l.filter(n=>n === l[i]).length === 1) {
            console.log(l[i]);
            return;
        }
    }
    
    console.log(l[0]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-島と橋
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    
    const N = ~~arg[0];
    const A = arg[1].split(" ").map(n=>~~n);
    
    const list = [0];

    for(let i=1; i<=N; i++) {
        list.push(list[i - 1] + A[i - 1]);
    }

    const sum = list[list.length - 1];
    const num = sum / N;
    
    let cnt = 0;
    
    for(let i=1; i<N; i++) {
        const left  = list[i];
        const right = sum - list[i];
    
        if (left !== (i * num) || right !== (N - i) * num) {
            cnt++;
        }
    }
    
    if (sum % N !== 0) {
        cnt = -1;
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```