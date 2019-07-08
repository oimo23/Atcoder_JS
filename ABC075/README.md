### ABC075
[問題ページ](https://atcoder.jp/contests/abc075/tasks)

### A-One out of Three
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ");
    
    for(let i=0; i<N.length; i++) {
        if(N.filter(n=>n==N[i]).length == 1) {
           console.log(N[i]);
           return;
       }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```