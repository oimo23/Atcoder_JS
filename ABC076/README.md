### ABC076
[問題ページ](https://atcoder.jp/contests/abc076/tasks)

### A-Rating Goal
```JavaScript
"use strict";

function main(arg) {
    const N = parseInt(arg.split("\n")[0]);
    const S = parseInt(arg.split("\n")[1]);
    console.log((S * 2) - N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Addition and Multiplication
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    const K = parseInt(arg.split("\n")[1]);
    let number = 1;
    
    for(let i=0; i<N; i++) {
        if(number * 2 < number + K) {
            number  = number * 2;
        } else {
            number += K;

        }
    }
    
    console.log(number);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```