### ABC042
[問題ページ](https://atcoder.jp/contests/abc042/tasks)

### A-和風いろはちゃんイージー
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).sort();
    
    console.log(S.join("") === "557" ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-文字列大好きいろはちゃんイージー / Iroha Loves Strings (ABC Edition)
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const L = parseInt(arg[0].split(" ")[1]);
    const S = arg.slice(1, N + 1);
    
    console.log(S.sort().join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-こだわり者いろはちゃん / Iroha's Obsession
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    let N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const kRegexp = new RegExp("["+arg[1].replace(" ","")+"]");
    
    while(kRegexp.test(String(N))) {
        N++;
    }
    
    let answer = N;
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```