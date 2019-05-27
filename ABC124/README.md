### ABC124
[問題ページ](https://atcoder.jp/contests/abc124/tasks)

### A-Buttons
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    let A = ~~arg[0].split(" ")[0];
    let B = ~~arg[0].split(" ")[1];
    
    let answer = 0;
    
    if(A > B) {
        answer += A;
        A--;
    } else {
        answer += B;
        B--;
    }
    
    if(A > B) {
        answer += A;
        A--;
    } else {
        answer += B;
        B--;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Great Ocean View
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const H = arg[1].split(" ").map(n=>~~n);
    
    let answer = 1;
    let heighest = H[0];
    
    for(let i=1; i<N; i++) {
        if(H[i] >= heighest) {
            answer++;
        }
        
        if(H[i] > heighest) {
            heighest = H[i];
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Coloring Colorfully
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("").map(n=>parseInt(n));
    
    let startWith0 = Array(S.length).fill(0).map((val,idx)=>idx % 2 !== 0 ? val = 1 : val = 0);
    let startWith1 = Array(S.length).fill(0).map((val,idx)=>idx % 2 !== 0 ? val = 0 : val = 1);
    
    let diffStartWith0 = 0;
    let diffStartWith1 = 0;

    S.forEach((val,idx) => {
        if(S[idx] !== startWith0[idx]) {
            diffStartWith0++;
        }
        
        if(S[idx] !== startWith1[idx]) {
            diffStartWith1++;
        }
    });
    
    console.log(Math.min(diffStartWith0, diffStartWith1));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```