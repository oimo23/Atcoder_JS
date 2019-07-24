### ABC052
[問題ページ](https://atcoder.jp/contests/abc052/tasks)

### A-Two Rectangles
```JavaScript
"use strict";
    
const main = arg => {
    const rectangles = arg.split("\n")[0].split(" ");
    const A = rectangles[0] * rectangles[1];
    const B = rectangles[2] * rectangles[3];
    console.log(Math.max(A, B));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Increment Decrement
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0];
    const S = arg[1];
    let answer  = [0];
    let counter = 0;
    
    for(let i in S) {
        if(S.charAt(i) === "I") {
            counter++;
            answer.push(counter);
        } else {
            counter--;
            answer.push(counter);
        }
    }
    
    console.log(Math.max(...answer));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Factors of Factorial
```JavaScript
"use strict";

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const MOD = 1e9 + 7;
    
    let cnt = [...Array(N + 1)].fill(0);
    
    for(let i=1; i<=N; i++) {
        let b = i;
        
        for(let j=2; j<=N; j++) {            
            while(b % j === 0) {
                b /= j;
                cnt[j]++;
            }
        }
    }
    
    let answer = 1;
    
    for(let i=2; i<=N; i++) {
        answer = answer * (cnt[i] + 1) % MOD;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```