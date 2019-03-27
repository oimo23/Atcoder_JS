### ABC068
[問題ページ](https://atcoder.jp/contests/abc068/tasks)

### A-ABCxxx
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    
    console.log("ABC" + N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Break Number
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    let list = [1, 2, 4, 8, 16, 32, 64];
    
    console.log(Math.max(...list.filter(n=>n<=N)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```