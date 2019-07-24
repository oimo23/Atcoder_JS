### ABC057
[問題ページ](https://atcoder.jp/contests/abc057/tasks)

### A-Remaining Time
```JavaScript
"use strict";
    
const main = arg => {
    arg     = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const A = arg[0];
    const B = arg[1];
    
    console.log(A + B >= 24 ? (A + B) - 24 : A + B);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Digits in Multiplication
```JavaScript
"use strict";

const main = arg => {
  arg = arg.trim().split("\n");
  const N = parseInt(arg[0]);
  
  let answer = Infinity;
  
  for(let i=1; i<=Math.sqrt(N); i++) {
      if(N % i === 0) {
          const f = Math.max(String(i).length, String(N / i).length);
          answer = Math.min(answer, f);
      }
  }
  
  console.log(answer);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```