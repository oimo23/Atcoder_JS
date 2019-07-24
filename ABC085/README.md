### ABC085
[問題ページ](https://atcoder.jp/contests/abc085/tasks)

### A-Already 2018
```JavaScript
"use strict";

const main = arg => {
    const date = arg.split("\n")[0].split("/");
    console.log("2018/" + date[1] + "/" + date[2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Kagami Mochi
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    const d = arg.split("\n").slice(1, N+1).map(n=>parseInt(n)).sort((a,b)=>b-a);
    
    const set = new Set(d);
    
    console.log(parseInt(set.size));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Otoshidama
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const Y = ~~arg[0].split(" ")[1];
    
    for(let i=0; i<=N; i++) {
        for(let j=0; j<=N; j++) {
            let k = N - i - j;
            
            if(k < 0) continue;
            
            let price = (10000 * i) + (5000 * j) + (1000 * k);
            let bills = ~~i + ~~j + ~~k;
            
            if(Y === price && N === bills) {
                console.log(`${i} ${j} ${k}`);
                return;
            }
        }
    }
    
    console.log("-1 -1 -1");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```