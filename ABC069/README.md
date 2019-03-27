### ABC069
[問題ページ](https://atcoder.jp/contests/abc069/tasks)

### A-K-City
```JavaScript
"use strict";

const main = arg => {
    const n = arg.split("\n")[0].split(" ")[0];
    const m = arg.split("\n")[0].split(" ")[1];
    
    console.log((n - 1) * (m - 1));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-i18n
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split("");
    const head = S[0];
    const tail = S[S.length - 1];
    
    S.shift();
    S.pop();
    
    console.log(head + S.length + tail);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```