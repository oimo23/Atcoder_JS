### ABC115
[問題ページ](https://atcoder.jp/contests/abc115/tasks)

### A-Christmas Eve Eve Eve
```JavaScript
const main = input => {
    input = parseInt(input);
    switch(input) {
      case 25:
        console.log("Christmas");
        break;
      case 24:
        console.log("Christmas Eve");
        break;
      case 23:
        console.log("Christmas Eve Eve");
        break;
      case 22:
        console.log("Christmas Eve Eve Eve");
        break;
    }
}
 
main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```

### B-Christmas Eve Eve
```JavaScript
"use strict";

const main = input => {
  input = input.split("\n");
 
  let n = parseInt(input[0], 10)
  let p = input.slice(1, n + 1).map(n => parseInt(n, 10))
 
  let top = p.reduce((n, m) => n >= m? n: m)
  let sum = p.reduce((n, m) => n + m)
 
  console.log(sum - (top / 2))
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```

### C-Christmas Eve
```JavaScript
"use strict";

const main = input => {
    input = input.split("\n");
    let temp = input[0].split(" ").map(x => parseInt(x));
    let N = temp[0];
    let K = temp[1];
    
    let h = input.slice(1, N+1).map(x => parseInt(x));
    h.sort((n,m)=> n-m);

    let min = Math.pow(10, 10);
    
    for( let  i=0; i<(N-K)+1 ; i++) {
        let tempMin = h[i+(K-1)] - h[i];
        min = Math.min(min, tempMin);
    }
    
    console.log(min);
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```