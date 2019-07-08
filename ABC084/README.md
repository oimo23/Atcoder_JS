### ABC084
[問題ページ](https://atcoder.jp/contests/abc084/tasks)

### A-New Year
```JavaScript
"use strict";

const main = arg => {
    console.log(48 - parseInt(arg.split("\n")[0]));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Postal Code
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    const S = arg.split("\n")[1];
    
    if(S.split("-")[0].length == A && S.split("")[A] == "-" && S.split("-")[1].length == B) {
        console.log("Yes");
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```