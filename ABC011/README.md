### ABC011
[問題ページ](https://atcoder.jp/contests/abc011/tasks)

### A-来月は何月？
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    
    console.log(N === 12 ? 1 : N + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-名前の確認
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("").map(n=>n.toLowerCase());
    
    S[0] = S[0].toUpperCase();
    
    console.log(S.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-123引き算
```JavaScript
"use strict"

const main = arg => {
  arg = arg.split("\n").map(n=>parseInt(n));
  const NGs = arg.slice(1, -1);
  let N = arg[0];
  let counter = 0;
  let result = true;

  NGs.forEach((NG) => {
    if (N === NG) result = false;
  })

  const canSubtract = (n) => {
    let judge = true;
    
    NGs.forEach((NG) => {
      if (n === NG) judge = false;
    })
    
    return judge;
  };

  while(N > 0 && counter < 100 && result) {
    if (canSubtract(N - 3)) {
      N -= 3;
      counter++;
    } else if (canSubtract(N - 2)) {
      N -= 2;
      counter++;
    } else if (canSubtract(N - 1)) {
      N -= 1;
      counter++;
    } else {
      result = false;
      break;
    }
  }

  result = (result && N <= 0) ? true :false;

  console.log(result ? 'YES' : 'NO');
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```