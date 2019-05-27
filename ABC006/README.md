### ABC006
[問題ページ](https://atcoder.jp/contests/abc006/tasks)

### A-AtCoder Crackers
```JavaScript
'use strict';

function main(arg) {
    console.log(arg.split(" ")[0] % arg.split(" ")[1] === 0 ? 0 : 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Cakes and Donuts
```JavaScript
'use strict';

function main(arg) {
    const N = parseInt(arg.split("\n")[0]);
    
    if(N < 4) {
        console.log("No");
        return;
    }
    
    if(N % 4 === 0 || N % 7 === 0 ) {
        console.log("Yes");
        return;
    }
    
    for(let i=0; i<N; i=i+4) {
        if((N - i) % 7 === 0) {
            console.log("Yes");
            return;
        }
    }
    
    for(let i=0; i<N; i=i+7) {
        if((N - i) % 4 === 0) {
            console.log("Yes");
            return;
        }
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```