### ABC070
[問題ページ](https://atcoder.jp/contests/abc070/tasks)

### A-Palindromic Number
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split("");
    const R = N.slice(0, N.length);
    
    console.log(N.join("") == R.reverse().join("") ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Two Switches
```JavaScript
"use strict";
    
const main = arg => {
    const times = arg.split("\n")[0].split(" ");
    
    const start = Math.max(times[0], times[2]);
    const end   = Math.min(times[1], times[3]);
    
    console.log(end - start > 0 ? end - start : 0);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```