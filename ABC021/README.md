### ABC021
[問題ページ](https://atcoder.jp/contests/abc021/tasks)

### A-足し算
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    
    console.log(N);
    
    for(let i=0; i<N; i++) {
        console.log(1);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-嘘つきの高橋くん
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const a = arg[1].split(" ")[0];
    const b = arg[1].split(" ")[1];
    
    const root = arg[3].split(" ");
    const set  = new Set(root);
    
    if(set.size === root.length && root.indexOf(b) === -1 && root.indexOf(a) === -1) {
        console.log("YES");
    } else {
        console.log("NO");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```