### ABC003
[問題ページ](https://atcoder.jp/contests/abc003/tasks)

### A-AtCoder社の給料
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" "));
    
    console.log((((N * (N + 1) / 2)) / N) * 10000);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AtCoderトランプ
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S1 = arg[0];
    const S2 = arg[1];
    const words = ["a", "t", "c", "o", "d", "e", "r"];
    
    for(let i in S1) {
        if(S1[i] !== S2[i] && S1[i] !== "@" && S2[i] !== "@") {
            console.log("You will lose");
            return;
        }
        
        if(S1[i] === "@" && S2[i] === "@") {
            continue;
        }
        
        if(S1[i] === "@") {
            if(words.indexOf(S2[i]) === -1) {
                console.log("You will lose");
                return;
            }
        }
        
        if(S2[i] === "@") {
            if(words.indexOf(S1[i]) === -1) {
                console.log("You will lose");
                return;
            }
        }
    }
    
    console.log("You can win");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-AtCoderプログラミング講座
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const R = arg[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    const selectedR = R.slice(-K);
    
    let answer = 0;
    
    for(let i in selectedR) {
        answer = (answer + selectedR[i]) / 2;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```