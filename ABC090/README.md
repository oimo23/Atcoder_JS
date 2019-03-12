### ABC090
[問題ページ](https://atcoder.jp/contests/abc090/tasks)

### A-Diagonal String
```JavaScript
"use strict";

function main(arg) {
    const letters = arg.split("\n").map(n=>n.split(""));
    console.log(letters[0][0] + letters[1][1] + letters[2][2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Palindromic Numbers
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    let cnt = 0;
    
    for(let i=A; i<=B; i++) {
        if(String(i) == String(i).split("").reverse().join("")) {
            cnt++;
        }
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```