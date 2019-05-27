### ABC025
[問題ページ](https://atcoder.jp/contests/abc025/tasks)

### A-25個の文字列
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S = arg[0].split("");
    const N = ~~arg[1];
    
    const a = Math.floor((N - 1) / 5);
    const b = (N - 1) % 5;
    
    console.log(S[a] + S[b]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-双子とスイカ割り
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const A = ~~arg[0].split(" ")[1];
    const B = ~~arg[0].split(" ")[2];
    
    const moves = arg.slice(1, N + 1);
    let answer = 0;
    
    for(let i in moves) {
        let direction = moves[i].split(" ")[0];
        let number = ~~moves[i].split(" ")[1];
        
        if(number < A) {
            number = A;
        } else if(number > B) {
            number = B;
        }
        
        if(direction === "West") {
            answer -= number;
        } else {
            answer += number;
        }
    }
    
    if(answer === 0) {
        console.log(0);
    } else if(answer > 0) {
        console.log("East " + answer); 
    } else {
        console.log("West " + (answer * -1));
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```