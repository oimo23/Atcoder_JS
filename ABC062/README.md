### ABC062
[問題ページ](https://atcoder.jp/contests/abc062/tasks)

### A-Grouping
```JavaScript
"use strict";

const main = arg => {
    const A = [1,3,5,7,8,10,12];
    const B = [4,6,9,11];
    
    const x = parseInt(arg.split("\n")[0].split(" ")[0]);
    const y = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if(x == y) {
        console.log("Yes");
        return;
    }
    
    if(A.indexOf(x) !== -1 && A.indexOf(y) !== -1) {
        console.log("Yes");
        return;
    }
    
    if(B.indexOf(x) !== -1 && B.indexOf(y) !== -1) {
        console.log("Yes");
        return;
    }
    
    console.log("No");
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Picture Frame
```JavaScript
"use strict";

const main = arg => {
    const H = parseInt(arg.split("\n")[0].split(" ")[0]);
    const W = parseInt(arg.split("\n")[0].split(" ")[1]);
    const pixel = arg.split("\n").slice(1, H + 1);
    
    let answer = [];
    
    answer[0] = [];
    answer[0].push("#".repeat(W + 2));
    
    for(let i=1; i<=H; i++) {
        answer[i] = [];
        answer[i].push("#" + pixel[i - 1] + "#");
    }

    answer[H + 1] = [];
    answer[H + 1].push("#".repeat(W + 2));
    
    console.log(answer.join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```