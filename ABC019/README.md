### ABC019
[問題ページ](https://atcoder.jp/contests/abc019/tasks)

### A-高橋くんと年齢
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const numbers = arg[0].split(" ").map(n=>parseInt(n));
    
    console.log(numbers.sort((a,b)=>a-b)[1]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-高橋くんと文字列圧縮
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    
    let answer = [];
    let last;
    let streak = 1;
    
    for(let i=0; i<S.length; i++) {
        if(last === S[i]) {
            streak++;
        } else {
            streak = 1;
        }
        
        if(S[i + 1] !== S[i]) {
            answer.push(S[i] + streak);
        }
        
        last = S[i];
    }
    
    console.log(answer.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```