### ABC038
[問題ページ](https://atcoder.jp/contests/abc038/tasks)

### A-お茶
```JavaScript
"use strict";

const main = arg => {
    const S = arg.split("\n")[0].split("");
    
    console.log(S.pop() === "T" ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ディスプレイ
```JavaScript
"use strict";
    
const main = arg => {
    const monitors = arg.trim().split("\n").map(n=>n.split(" "));
    
    if(
        monitors[0][0] === monitors[1][0] || monitors[0][0] === monitors[1][0] ||
        monitors[0][1] === monitors[1][0] || monitors[0][1] === monitors[1][1]
    ) {
        console.log("YES");
        return;
    }

    console.log("NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```


### C-単調増加
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const A = arg[1].split(" ").map(n=>parseInt(n));
    
    let sum = 0;
    
    for(let left=0, right=0; left<N; left++) {
        if(right < left) right = left;
        
        while(right < N && A[right] < A[right+1]) {
            right++;
        }
        
        sum += right - left + 1;
    }
    
    console.log(sum);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```