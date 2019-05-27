### ABC038
[問題ページ](https://atcoder.jp/contests/abc038/tasks)

### A-お茶
```JavaScript
"use strict";

const main = arg => {
    const S = arg.split("\n")[0].split("");
    
    console.log(S.pop() === "T" ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ディスプレイ
```JavaScript
"use strict";
    
const main = arg => {
    const monitors = arg.trim().split("\n").map(n=>n.split(" "));
    
    if(
        monitors[0][0] === monitors[1][0] || monitors[0][0] === monitors[1][0] ||
        monitors[0][1] === monitors[1][0] || monitors[0][1] === monitors[1][1]
    ) {
        console.log("YES");
        return;
    }

    console.log("NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```