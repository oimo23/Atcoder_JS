### ABC095
[問題ページ](https://atcoder.jp/contests/abc095/tasks)

### A-Day of Takahashi
```JavaScript
"use strict";

const main = arg => {
    const date = arg.split("\n")[0].split(" ").join("");
    const memo = [11,22,33,44,55,66,77,88,99,1010,1111,1212];
    
    console.log(memo.filter(n=>n<=date).length);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Maximum Sum
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    const K = arg.split("\n")[1];
    const target = Math.max(...N) * Math.pow(2, K);
    N.pop();
    N.push(target);
    
    console.log(N.reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```