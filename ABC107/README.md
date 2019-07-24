### ABC107
[問題ページ](https://atcoder.jp/contests/abc107/tasks)

### A-Train
```JavaScript
"use strict";

const main = arg => {
    console.log((arg.split(" ")[0] - arg.split(" ")[1]) + 1)
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Grid Compression
```JavaScript
'use strict'

const main = arg => {
  arg = arg.trim().split('\n');
  const H = arg[0].split(' ')[0];
  let W   = arg[0].split(' ')[1];
  const a = arg.slice(1);
  let ans = [];
  
  for (let i = 0; i < H; i++) {
    if (a[i].indexOf('#') != -1) {
      ans.push(a[i]);
    }
  }

  for (let i = 0; i < W; i++) {
    let cnt = 0;
    
    for (let j = 0; j < ans.length; j++) {
      if (ans[j][i] == '#') {
        cnt++;
      }
    }

    if (cnt == 0) {
      for (let j = 0; j < ans.length; j++) {
        let tmp = ans[j].split('');
        tmp.splice(i, 1);
        ans[j] = tmp.join('');
      }
      
      i--;
      W--;
    }
  }
  
  for (let i = 0; i < ans.length; i++) {
    console.log(ans[i]);
  }
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'))

```

### C-Candles
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const x = arg[1].split(" ").map(n=>parseInt(n));
    
    const list = [];
    
    for(let i=0; i<=N - K; i++) {
        let left  = x[i];
        let right = x[~~i + K - 1];
        
        if(Math.abs(left) < Math.abs(right)) {
            list.push(Math.abs(left) + Math.abs(right - left));
        } else {
            list.push(Math.abs(right) + Math.abs(right - left));
        }
    }
    
    console.log(Math.min(...list));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```