### ABC108
[問題ページ](https://atcoder.jp/contests/abc108/tasks)

### A-Pair
```JavaScript
"use strict";

const main = arg => {
    arg = parseInt(arg);
    const evenCnt = Math.floor(arg / 2);
    const oddCnt  = arg - evenCnt;
    console.log(evenCnt * oddCnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Ruined Square
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const A = parseInt(arg[0].split(" ")[0]);
    const B = parseInt(arg[0].split(" ")[1]);
    const C = parseInt(arg[0].split(" ")[2]);
    const D = parseInt(arg[0].split(" ")[3]);
    
    const X = C - A;
    const Y = D - B;

    console.log((C - Y) + " " + (D + X) + " " + (A - Y) + " " + (B + X));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Triangular Relationship
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    let answer = 0;
    
    if(K % 2 !== 0) {
        // 奇数のとき
        // Kで割り切れる個数の3乗
        for(let i=1; i<=N; i++) {
            if(i % K === 0) answer++;
        }
        
        answer = Math.pow(answer, 3);
    } else {
        // 偶数のとき
        // Kで割り切れる個数の3乗と
        // K / 2の個数の3乗を足したもの 
        let half = 0;
        let mod0 = 0;
        
        for(let i=1; i<=N; i++) {
            if(i % K === K / 2) {
                half++;
            }
            
            if(i % K === 0) {
                mod0++;
            }
        }
        
        answer += Math.pow(half, 3);
        answer += Math.pow(mod0, 3);
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```