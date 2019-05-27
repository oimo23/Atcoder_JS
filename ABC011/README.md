### ABC011
[問題ページ](https://atcoder.jp/contests/abc011/tasks)

### A-来月は何月？
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    
    console.log(N === 12 ? 1 : N + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-名前の確認
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("").map(n=>n.toLowerCase());
    
    S[0] = S[0].toUpperCase();
    
    console.log(S.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```