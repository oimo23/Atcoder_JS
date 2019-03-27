### ABC042
[問題ページ](https://atcoder.jp/contests/abc042/tasks)

### A-和風いろはちゃんイージー
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).sort();
    
    console.log(S.join("") === "557" ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```