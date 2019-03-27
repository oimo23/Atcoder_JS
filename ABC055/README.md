### ABC055
[問題ページ](https://atcoder.jp/contests/abc055/tasks)

### A-Restaurant
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    
    console.log((800*N) - (Math.floor(N/15)*200));

}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```