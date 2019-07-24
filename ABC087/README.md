### ABC087
[問題ページ](https://atcoder.jp/contests/abc087/tasks)

### A-Buying Sweets
```JavaScript
"use strice";

const main = arg => {
    const price   = parseInt(arg.split("\n")[0]);
    const cake    = parseInt(arg.split("\n")[1]);
    const donut   = parseInt(arg.split("\n")[2]);
    console.log((price - cake) % donut);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Coins
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const A = ~~arg[0];
    const B = ~~arg[1];
    const C = ~~arg[2];
    
    const X = ~~arg[3];
    let answer = 0;
    
    for(let i=0; i<=A; i++) {
        for(let j=0; j<=B; j++) {
            for(let k=0; k<=C; k++) {
                if(500 * i + 100 * j + 50 * k === X) {
                   answer++; 
                }
            }
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Candies
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N     = ~~arg[0];
    const table = arg.slice(1, 3).map(n=>n.split(" ").map(l=>~~l));
    
    let cnt = 0;
    
    for(let down=0; down<N; down++) {
        let sum = 0;
        
        for(let i=0; i<N; i++) {
            if(i <= down) {
                sum += table[0][i];
            }
            if(i >= down) {
                sum += table[1][i];
            }
        }
        
        cnt = Math.max(cnt, sum);
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```