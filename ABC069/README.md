### ABC069
[問題ページ](https://atcoder.jp/contests/abc069/tasks)

### A-K-City
```JavaScript
"use strict";

const main = arg => {
    const n = arg.split("\n")[0].split(" ")[0];
    const m = arg.split("\n")[0].split(" ")[1];
    
    console.log((n - 1) * (m - 1));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-i18n
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split("");
    const head = S[0];
    const tail = S[S.length - 1];
    
    S.shift();
    S.pop();
    
    console.log(head + S.length + tail);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-4-adjacent
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ").map(n=>parseInt(n));

    let odd  = 0;
    let even = 0;
    let four = 0;
    
    for(let i=0; i<N; i++) {
        if(a[i] % 4 === 0) {
            four++;
        } else if(a[i] % 2 === 0) {
            even++;
        } else {
            odd++;
        }
    }
    
    let answer = "No";
    
    // 4の倍数が奇数より多い
    if(odd <= four) {
        answer = "Yes";
    // 4の倍数 + 1が奇数と同じ かつ 2の倍数はない
    } else if(four + 1 === odd && even === 0) {
        answer = "Yes";
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```