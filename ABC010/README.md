### ABC010
[問題ページ](https://atcoder.jp/contests/abc010/tasks)

### A-ハンドルネーム
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S = arg[0];
    
    console.log(S + "pp");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-花占い
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const a = arg[1].split(" ").map(n=>~~n);
    
    let cnt = 0;
    
    for(let i=0; i<N; i++) {
        while(a[i] % 3 === 2 || a[i] % 2 === 0) {
            a[i]--;
            cnt++;
        }
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-浮気調査
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const sX = parseInt(arg[0].split(" ")[0]);
    const sY = parseInt(arg[0].split(" ")[1]);
    const eX = parseInt(arg[0].split(" ")[2]);
    const eY = parseInt(arg[0].split(" ")[3]);
    const T  = parseInt(arg[0].split(" ")[4]);
    const V  = parseInt(arg[0].split(" ")[5]);
    
    const N = parseInt(arg[1]);
    const girls = arg.slice(2, N + 2);
    
    for(let i in girls) {
        const gX  = girls[i].split(" ")[0];
        const gY  = girls[i].split(" ")[1];
        
        const abs = Math.sqrt((Math.pow((gX - sX), 2) + Math.pow((gY - sY), 2))) +
                    Math.sqrt((Math.pow((eX - gX), 2) + Math.pow((eY - gY), 2)));

        if(abs <= T * V) {
            console.log("YES");
            return;
        }
    }
    
    console.log("NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
