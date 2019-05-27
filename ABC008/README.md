### ABC008
[問題ページ](https://atcoder.jp/contests/abc008/tasks)

### A-アルバム
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = arg[0].split(" ")[0];
    const B = arg[0].split(" ")[1];
    
    console.log((B - A) + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-投票
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    const S = arg.slice(1, N + 1);
    
    let most;
    let max  = 0;
    let temp = 0;
    
    for(let i in S) {
        temp = 0;
        
        for(let j in S) {
            if(S[i] === S[j]) {
                temp++;
            }   
        }
        
        if(temp > max) {
            max  = temp;
            most = S[i];
        }
    }
    
    console.log(most);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```