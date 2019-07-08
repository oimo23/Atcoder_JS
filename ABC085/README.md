### ABC085
[問題ページ](https://atcoder.jp/contests/abc085/tasks)

### A-Already 2018
```JavaScript
"use strict";

const main = arg => {
    const date = arg.split("\n")[0].split("/");
    console.log("2018/" + date[1] + "/" + date[2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Kagami Mochi
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    const d = arg.split("\n").slice(1, N+1).map(n=>parseInt(n)).sort((a,b)=>b-a);
    
    const set = new Set(d);
    
    console.log(parseInt(set.size));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```