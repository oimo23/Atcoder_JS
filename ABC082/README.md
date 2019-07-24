### ABC082
[問題ページ](https://atcoder.jp/contests/abc082/tasks)

### A-Round Up the Mean
```JavaScript
"use strict";

const main = arg => {
    arg = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    console.log(Math.ceil((arg[0] + arg[1]) / 2));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Two Anagrams
```JavaScript
"use strict";
    
const main = arg => {
    const s = arg.split("\n")[0].split("").sort().join("");
    const t = arg.split("\n")[1].split("").sort().reverse().join("");
    
    if(s < t) {
        console.log("Yes");   
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Good Sequence
```JavaScript
"use strict";

const main = arg => {
  arg = arg.trim().split("\n");
  const N = parseInt(arg[0]);
  const A = arg[1].split(" ").map(n=>parseInt(n));
  
  let answer = 0;
  
  const map = [...Array(100001)].fill(0);
  
  for(let i=0; i<N; i++) {
      if(A[i] > 100000) {
        answer++;
      } else {
        map[A[i]]++;
      }
  }
  
  for(let i=0; i<map.length; i++) {
    if(i > map[i]) answer += map[i];
    if(i < map[i]) answer += map[i] - i;
  }
  
  console.log(answer);
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```