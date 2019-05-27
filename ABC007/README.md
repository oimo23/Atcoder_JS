### ABC007
[問題ページ](https://atcoder.jp/contests/abc007/tasks)

### A-植木算
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0].split(" ");
    
    console.log(N - 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-辞書式順序
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0];
    
    if(S === "a") {
        console.log(-1);
    } else {
        console.log("a");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-幅優先探索
```JavaScript
"use strict";

const main = arg => {
    arg = arg.split("\n");
    
    const R = parseInt(arg[0].split(" ")[0]);
    const C = parseInt(arg[0].split(" ")[1]);
    
    const startR = parseInt(arg[1].split(" ")[0]) - 1;
    const startC = parseInt(arg[1].split(" ")[1]) - 1;
    
    const goalR = parseInt(arg[2].split(" ")[0]) - 1;
    const goalC = parseInt(arg[2].split(" ")[1]) - 1;
    
    const table = arg.slice(3, 3 + (R + 1)).map(n=>n.split(""));
    const min   = [...Array(R)].map(n=>[...Array(C)].fill("*"));
    
    const dx = [1, 0, -1, 0];
    const dy = [0, 1, 0, -1];
    
    const bfs = () => {
        const queue = [];
        
        queue.push([startR, startC]);
        min[startR][startC] = 0;
        
        // Queue に残りがある限りループする
        while(queue.length > 0) {
            const p = queue.shift();
            
            // ゴールに到着しているならbreak
            if(p[0] === goalR && p[1] === goalC) {
                break;
            }
            
            // 右、下、左、上の順でチェック
            for(let i=0; i<4; i++) {
                const nx = p[0] + dx[i];
                const ny = p[1] + dy[i];
                
                // はみ出し、壁衝突を考慮する
                if(nx < 0 || R <= nx) continue;
                if(ny < 0 || C <= ny) continue;
                if(table[nx][ny] === '#') continue;
                if(min[nx][ny] !== '*') continue;
                
                // 新しいポジションへの移動は現地点への最短経路+1となる
                queue.push([nx, ny]);
                min[nx][ny] = min[p[0]][p[1]] + 1;
            }
        }
        
        return min[goalR][goalC];
    }
    
    const answer = bfs();
    console.log(answer);
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
