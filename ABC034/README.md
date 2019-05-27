### ABC034
[問題ページ](https://atcoder.jp/contests/abc034/tasks)

### A-テスト
```JavaScript
"use strict";

const main = arg => {
    const X = parseInt(arg.split("\n")[0].split(" ")[0]);
    const Y = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    console.log(Y > X ? "Better" : "Worse");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ペア
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    
    console.log(N % 2 === 0 ? N - 1 : N + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```