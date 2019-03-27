### ABC059
[問題ページ](https://atcoder.jp/contests/abc059/tasks)

### A-Three-letter acronym
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split(" ").map(n=>n.toUpperCase());
    console.log(S[0].split("")[0] + S[1].split("")[0] + S[2].split("")[0]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Comparison
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = parseInt(arg[0]);
    const B = parseInt(arg[1]);
    
    if(A === B) {
        console.log("EQUAL");
        return;
    }
    
    console.log(A > B ? "GREATER" : "LESS");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```