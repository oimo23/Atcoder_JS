### ABC099
[問題ページ](https://atcoder.jp/contests/abc099/tasks)

### A-ABD
```JavaScript
"use strict";

const main = arg => {
    console.log(arg.split("\n")[0].length <= 3 ? "ABC" : "ABD");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Stone Monument
```JavaScript
"use strict";

const main = arg => {
    const a = parseInt(arg.split("\n")[0].split(" ")[0]);
    const b = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    const diff = b - a;
    let indexB = 0;
    
    for(let i=0; i<=diff; i++) {
        indexB += i;
    }
    
    console.log(indexB - b);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Strange Bank
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    
    const MAX = 110000;
    let dp = [...Array(N)];
    
    for(let i=0; i<MAX; i++) {
        dp[i] = Infinity;
    }
    
    dp[0] = 0;
    
    for(let i=1; i<=N; i++) {
        for(let pow6=1; pow6<=i; pow6 *= 6) {
            dp[i] = Math.min(dp[i], dp[i - pow6] + 1);
        }
        
        for(let pow9=1; pow9<=i; pow9 *= 9) {
            dp[i] = Math.min(dp[i], dp[i - pow9] + 1);
        }
    }

    console.log(dp[N]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```