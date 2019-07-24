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

### C-Grid Repainting 2
```JavaScript
"use strict"

const main = arg => {
  arg = arg.trim().split("\n");
  const H = parseInt(arg[0].split(" ")[0]);
  const W = parseInt(arg[0].split(" ")[1]);
  
  const tiles = arg.slice(1, H + 1).map(n=>n.split(""));
  
  const dx = [1, 0, -1, 0];
  const dy = [0, 1, 0, -1];
  
  for(let i in tiles) {
      for(let j in tiles[i]) {
          let cnt = 0;
          
          for(let k=0; k<4; k++) {
              let nx = dx[k] + parseInt(j);
              let ny = dy[k] + parseInt(i);
              
              if(ny < 0 || ny > H - 1) continue;
              if(nx < 0 || nx > W - 1) continue;
             
              if(tiles[ny][nx] === ".") {
                  cnt++;
              }
          }
          
          if(tiles[i][j] === "#" && cnt === 4) {
              console.log("No");
              return;
          }
      }
   }
   
   console.log("Yes");
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```