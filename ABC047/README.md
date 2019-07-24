### ABC047
[問題ページ](https://atcoder.jp/contests/abc047/tasks)

### A-キャンディーと2人の子供
```JavaScript
"use strict";
    
const main = arg => {
	const packs = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).sort((a,b)=>b-a);
	console.log(packs[0] === packs[1] + packs[2] ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-すぬけ君の塗り絵 2 イージー / Snuke's Coloring 2 (ABC Edit)
```JavaScript
"use strict";

const main = arg => {
  arg = arg.trim().split("\n");

  const w = ~~(arg[0].split(" ")[0]);
  const h = ~~(arg[0].split(" ")[1]);
  const n = ~~(arg[0].split(" ")[2]);

  const points = arg.slice(1, n + 1).map(l => l.split(" ").map(n => ~~n));
  const list = [...Array(h)].map(l => [...Array(w)].fill(0));

  for(const point of points) {
    const x = point[0];
    const y = point[1];
    const a = point[2] - 1;

    const fromH = [0, 0, 0, y];
    const toH   = [h, h, y, h];
    const fromW = [0, x, 0, 0];
    const toW   = [x, w, w, w];

    for(let i = fromH[a]; i < toH[a]; i++) {
      for(let j = fromW[a]; j < toW[a]; j++) {
        list[i][j] = 1;
      }
    }
  }

  let cnt = 0;
  
  for(let i = 0; i < h; i++) {
    for(let j = 0; j < w; j++) {
      if(list[i][j] === 0) cnt++;
    }
  }

  console.log(cnt);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

```

### C-一次元リバーシ / 1D Reversi
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    const list = [];
    
    let last;
    
    for(let i in S) {
        if(S[i] !== last) {
            list.push(S[i]);
        }
        
        last = S[i];
    }

    console.log(list.join("").length - 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```