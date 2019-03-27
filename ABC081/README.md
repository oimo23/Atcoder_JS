### ABC081
[問題ページ](https://atcoder.jp/contests/abc081/tasks)

### A-Placing Marbles
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0].split("");
    console.log(N.filter(n=>n=="1").length);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Shift only
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    let A = arg.split("\n")[1].split(" ");
    let flg = true;
    let cnt = 0;
    
    while(flg) {
        if(A.filter(n=>n%2==0).length !== N) {
            flg = false;
        } else {
            A = A.map(n=>n / 2);
            cnt++;
        }
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```