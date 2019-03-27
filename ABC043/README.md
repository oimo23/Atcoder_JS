### ABC043
[問題ページ](https://atcoder.jp/contests/abc043/tasks)

### A-キャンディーとN人の子供イージー
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    
    console.log((N * (N + 1)) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```