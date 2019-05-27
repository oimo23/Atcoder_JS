### ABC013
[問題ページ](https://atcoder.jp/contests/abc013/tasks)

### A-A
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const S = arg[0];
    const alphabet = ["A", "B", "C", "D", "E"];
    
    console.log(alphabet.indexOf(S) + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-錠
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const a = ~~arg[0];
    const b = ~~arg[1];
    
    console.log(Math.min(Math.abs(b - a), 10 + Math.min(a, b) - Math.max(a, b)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
