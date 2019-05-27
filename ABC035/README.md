### ABC035
[問題ページ](https://atcoder.jp/contests/abc035/tasks)

### A-テレビ
```JavaScript
"use strict";

const main = arg => {
    const W = arg.split("\n")[0].split(" ")[0];
    const H = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if((W / 4) * 3 === H) {
        console.log("4:3");
    } else {
        console.log("16:9");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ドローン
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    const T = ~~arg[1];
    
    const up    = S.filter(n=>n==="U").length;
    const down  = S.filter(n=>n==="D").length;
    const right = S.filter(n=>n==="R").length;
    const left  = S.filter(n=>n==="L").length;
    const q     = S.filter(n=>n==="?").length;
    
    // 縦の移動距離
    const vertical = Math.abs(up - down);
    // 横の移動距離
    const horizontal = Math.abs(right - left);
    
    let answer;
    
    if(T === 1) {
        answer = vertical + horizontal + q;
    } else if(vertical + horizontal >= q){
        answer = vertical + horizontal - q;
    } else {
        answer = (q - vertical + horizontal) % 2;
    }
    
    console.log(Math.max(answer, 0));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```