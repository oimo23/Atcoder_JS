### ABC099
[問題ページ](https://atcoder.jp/contests/abc099/tasks)

### A-ABD
```JavaScript
"use strict";

function main(arg) {
    console.log(arg.split("\n")[0].length <= 3 ? "ABC" : "ABD");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Stone Monument
```JavaScript
"use strict";

function main(arg) {
    const a = parseInt(arg.split("\n")[0].split(" ")[0]);
    const b = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    const diff = b - a;
    let indexB = 0;
    
    for(let i=0; i<=diff; i++) {
        indexB += i;
    }
    
    console.log(indexB - b);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```