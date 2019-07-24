### ABC076
[問題ページ](https://atcoder.jp/contests/abc076/tasks)

### A-Rating Goal
```JavaScript
"use strict";

const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    const S = parseInt(arg.split("\n")[1]);
    console.log((S * 2) - N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Addition and Multiplication
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    const K = parseInt(arg.split("\n")[1]);
    let number = 1;
    
    for(let i=0; i<N; i++) {
        if(number * 2 < number + K) {
            number  = number * 2;
        } else {
            number += K;

        }
    }
    
    console.log(number);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Dubious Document 2
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0];
    const T = arg[1];
    
    for(let i=S.length - T.length; i>=0; i--) {
        let flag = true;
        let sub  = S.substr(i, T.length);

        for(let j=0; j<T.length; j++) {
            if(sub.charAt(j) !== T.charAt(j) && sub.charAt(j) !== "?") {
                flag = false;
                break;
            }
        }
        
        if(flag === true) {
            let answer = S.substring(0, i) + T + S.substring(parseInt(i) + T.length);
            answer = answer.replace(/\?/g, "a");
            console.log(answer);
            return;
        }
    }
    
    console.log("UNRESTORABLE");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```