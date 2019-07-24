### ABC092
[問題ページ](https://atcoder.jp/contests/abc092/tasks)

### A-Traveling Budget
```JavaScript
"use strict";

const main = arg => {
    arg     = arg.split("\n");
    const A = parseInt(arg[0]);
    const B = parseInt(arg[1]);
    const C = parseInt(arg[2]);
    const D = parseInt(arg[3]);
    
    console.log(Math.min(A,B) + Math.min(C,D));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Chocolate
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0];
    const D = arg[1].split(" ")[0];
    const X = arg[1].split(" ")[1];
    const A = arg.slice(2).map(n=>parseInt(n));
    
    let original = 0;
    
    for(let i=0; i<A.length; i++) {
        for(let j=0; (j * A[i]) + 1 <= D; j++) {
            original++;
        }
    }
    
    console.log(parseInt(original) + parseInt(X));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Traveling Plan
```JavaScript
"use strict"

const main = arg => {
  arg = arg.trim().split("\n");
  const N = parseInt(arg[0]);
  const s = arg[1].split(" ").map(n=>parseInt(n));

  const points = [0, ...s, 0];
  const diff   = [];
  const answer = [];

  points.forEach((p, i, self) => {
    if (i < self.length - 1) diff.push(self[i + 1] - self[i]);
  });

  const sum = diff.map(n=>Math.abs(n)).reduce((a,b) =>a+b);

  for(let i=1; i<points.length - 1; i++) {
    const skipped = Math.abs(points[i - 1] - points[i + 1]);
    const stepped = Math.abs(points[i - 1] - points[i]) + Math.abs(points[i] - points[i + 1]);

    const changed = skipped - stepped;

    answer.push(sum + changed);
  }

  console.log(answer.join("\n"));
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```