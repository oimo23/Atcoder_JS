### ABC054
[問題ページ](https://atcoder.jp/contests/abc054/tasks)

### A-One Card Poker
```JavaScript
"use strict";
    
const main = arg => {
    let A = parseInt(arg.split("\n")[0].split(" ")[0]);
    let B = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if(A == 1) A = 14;
    if(B == 1) B = 14;
    
    if(A == B) {
        console.log("Draw");
    } else if(A > B) {
        console.log("Alice")
    } else {
        console.log("Bob")
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-One-stroke Path
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const ab = arg.slice(1, M + 1).map(n=>n.split(" ").map(l=>parseInt(l)));
    
    // グラフ用の2次元配列を作る
    const mx = [...Array(N)].map(n=>[...Array(N)].fill(0));
    
    for(let i in ab) {
        const from = ab[i][0] - 1;
        const to   = ab[i][1] - 1;
        
        mx[from][to] = 1;
        mx[to][from] = 1;
    }
    
    let sum = 0;

    const dfs = (v, visited) => {
        if (visited.every(v=>v===true)) sum++;
        
        for (let i=0; i<N; i++) {
          if (mx[v][i] === 0) continue;
          if (visited[i]) continue;
        
          visited[i] = true;
          dfs(i, visited);
          visited[i] = false;
        }
        
        return;
    }
    
    const visited = [true, ...[...Array(N - 1)].map(n=>false)];
    dfs(0, visited);
    
    console.log(sum);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```