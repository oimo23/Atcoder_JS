### ABC113
[問題ページ](https://atcoder.jp/contests/abc113/tasks)

### A-Discount Fare
```JavaScript
const main = arg => {
    const fares = arg.split(" ").map(n => parseInt(n));
    console.log(fares[0] + (fares[1] / 2))
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Palace
```JavaScript
"use strict";

const main = arg => {
    const tmp = arg.split("\n");
    const N = parseInt(tmp[0]);
    const T = parseInt(tmp[1].split(" ")[0]);
    const A = parseInt(tmp[1].split(" ")[1]);
    const H = tmp[2].split(" ").map(n=>parseInt(n));
    let diffs = [];
    
    for(let i=0; i<H.length; i++) {
        const H_ave = T - (H[i] * 0.006);
        diffs.push(Math.abs(A - H_ave));
    }
    
    const minDiff = Math.min(...diffs);
    let answer = diffs.indexOf(minDiff);
    
    console.log(answer + 1);
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```