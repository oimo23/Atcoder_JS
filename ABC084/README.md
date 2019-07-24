### ABC084
[問題ページ](https://atcoder.jp/contests/abc084/tasks)

### A-New Year
```JavaScript
"use strict";

const main = arg => {
    console.log(48 - parseInt(arg.split("\n")[0]));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Postal Code
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    const S = arg.split("\n")[1];
    
    if(S.split("-")[0].length == A && S.split("")[A] == "-" && S.split("-")[1].length == B) {
        console.log("Yes");
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Special Trains
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    let C = [];
    let S = [];
    let F = [];
    
    for(let i=1; i<N; i++) {
        let temp = arg[i].split(" ").map(n=>parseInt(n));
        C[i-1] = temp[0];
        S[i-1] = temp[1];
        F[i-1] = temp[2];
    }
    
    let answer  = [];
    
    for(let i=0; i<N; i++) {
        let time  = 0;
        time += S[i] + C[i];
        
        if(i === N - 1) {
            answer.push(0)
            break;
        }
        
        for(let j=parseInt(i)+1; j<N-1; j++) {
            if(time <= S[j]) {
                time = S[j] + C[j];
            } else {
                let temp = S[j] + F[j];
                
                while(temp < time) {
                    temp += F[j];
                }

                time = temp + C[j]; 
            }
        }
        
        answer.push(time);
    }

    console.log(answer.join("\n"))
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```