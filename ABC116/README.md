### ABC116
[問題ページ](https://atcoder.jp/contests/abc116/tasks)

### A-Right Triangle
```JavaScript
'use strict'

function main(arg) {
    const temp = arg.split(" ");
    console.log((temp[0] * temp[1]) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Collatz Problem
```JavaScript
'use strict';

function main(arg) {
    let s = parseInt(arg);
    let memo  = new Set();
    let cnt = 1;
    
    memo.add(s);
    
    while(true) {
        cnt++;
        if(s % 2 === 0) {
            s = s / 2;
            if(memo.has(s)) {
                console.log(cnt);
                break;
            }
            memo.add(s);
        } else {
            s = (s * 3) + 1;
            if(memo.has(s)) {
                console.log(cnt);
                break;
            }
            memo.add(s);
        }
    }
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```