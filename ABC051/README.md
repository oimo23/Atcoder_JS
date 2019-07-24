### ABC051
[問題ページ](https://atcoder.jp/contests/abc051/tasks)

### A-Haiku
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split(",").join(" ");

    console.log(S);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Sum of Three Integers
```JavaScript
'use strict'

const main = arg => {
    arg = arg.trim().split("\n")
    const K = parseInt(arg[0].split(" ")[0]);
    const S = parseInt(arg[0].split(" ")[1]);
    
    let answer = 0;
    
    for(let i=0; i<=K; i++) {
        for(let j=0; j<=K; j++) {
            let z = S - i - j;
            
            if(0 <= z && z <= K) {
                answer++;
            }
        }
    }
    
    console.log(answer);
}

main(require('fs').readFileSync('/dev/stdin', 'utf-8'))

```