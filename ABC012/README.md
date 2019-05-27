### ABC012
[問題ページ](https://atcoder.jp/contests/abc012/tasks)

### A-スワップ
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = arg[0].split(" ")[0];
    const B = arg[0].split(" ")[1];
    
    console.log(B + " " + A);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-入浴時間
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    
    let h = Math.floor(N / 3600);
    let m = Math.floor((N % 3600) / 60);
    let s = N - (h * 3600) - (m * 60);
    
    if(h < 10) {
        h = "0" + h;
    }
    
    if(m < 10) {
        m = "0" + m;
    }
    
    if(s < 10) {
        s = "0" + s;
    }
    
    console.log(`${h}:${m}:${s}`);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-九九足し算
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    const diff = 2025 - N; 
    
    for(let i=1; i<10; i++) {
        for(let j=1; j<10; j++) {
            if((i * j) === diff) {
                console.log(i + " x " + j);
            }
        }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
