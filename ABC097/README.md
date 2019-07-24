### ABC097
[問題ページ](https://atcoder.jp/contests/abc097/tasks)

### A-Colorful Transceivers
```JavaScript
"use strict";

const main = arg => {
    const positions = arg.split("\n")[0].split(" ").slice(0,3);
    const limit     = arg.split("\n")[0].split(" ")[3];

    
    if(Math.abs(positions[2] - positions[0]) <= limit) {
        console.log("Yes");
        return;
    }
    
    if( (Math.abs(positions[1] - positions[0]) <= limit) &&
        (Math.abs(positions[2] - positions[1]) <= limit) ) {
        console.log("Yes");
        return;
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Exponential
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    const powerOf = [1]; 
    
    for(let i=2; i<=32; i++) {
        let pow = 2;
        while(Math.pow(i, pow) <= N) {
            powerOf.push(Math.pow(i,pow));
            pow++;
        }
    }
    
    console.log(Math.max(...powerOf));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-K-th Substring
```JavaScript
"use strict"

const main = arg => {
  arg = arg.trim().split("\n");
  const str = arg[0];
  const len = str.length;
  const k   = parseInt(arg[1]);

  const initials = [...new Set(str.split(''))].sort();
  let index = 0;
  const dic = new Set();

  while(dic.size < k) {
    for(let i=0; i<len; i++) {
      let j = 1;
      if(str.slice(i, i + j) !== initials[index]) continue;

      while(i + j <= len && j <= 5) {
        dic.add(str.slice(i, i + j));
        j += 1;
      }
    }
    
    index++;
  }
  
  const ans = [...dic].sort()[k - 1];
  console.log(ans);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```