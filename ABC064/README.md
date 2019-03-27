### ABC064
[問題ページ](https://atcoder.jp/contests/abc064/tasks)

### A-RGB Cards
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ").join("");
    
    console.log(N % 4 === 0 ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```