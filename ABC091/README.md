### ABC091
[問題ページ](https://atcoder.jp/contests/abc091/tasks)

### A-Two Coins
```JavaScript
"use strict";

const main = arg => {
    const coins = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    console.log(coins[0] + coins[1] >= coins[2] ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Two Colors Card Game
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const blueN = parseInt(arg[0]);
    const blueS = arg.slice(1,blueN + 1);
    const redN  = parseInt(arg[blueN + 1]);
    const redS  = arg.slice(blueN+2);

    const set = new Set(redS.concat(blueS));
    let answer = [];

    set.forEach(item => {
        let temp = 0;
        let foundInBlue = blueS.filter(n=>n==item).length;
        let foundInRed  = redS.filter(n=>n==item).length;
        
        if(foundInBlue > 0) {
            temp += foundInBlue;
        }
        
        if(foundInRed > 0) {
            temp -= foundInRed;
        }
        
        answer.push(temp);
    })
    
    console.log(Math.max(...answer) > 0 ? Math.max(...answer) : 0);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-2D Plane 2N Points
```JavaScript
"use strict"

const main = arg => {
  arg = arg.trim().split("\n");
  const N = parseInt(arg[0]);

  arg = arg.slice(1, (2 * N) + 1).map(n=>n.split(" ").map(l=>parseInt(l))).map(xy => {
    return {x: xy[0], y: xy[1]}
  });

  const red  = arg.slice(0, N);
  const blue = arg.slice(N);
  const paired = [...Array(N)].fill(0);

  blue.sort((a, b) => a.x - b.x);

  for (let i=0; i<N; i++) {
    let max_y = -1;
    let idx = '';

    for (let j = 0; j < N; j++) {
      if(red[j].x >= blue[i].x) continue;
      if(red[j].y >= blue[i].y) continue;
      if(paired[j] === 1)       continue;
      if(max_y >= red[j].y)     continue;

      max_y = red[j].y;
      idx = j;
    }

    if (idx !== '') paired[idx] = 1;
  }

  const ans = paired.filter(n=>n===1).length;

  console.log(ans);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```