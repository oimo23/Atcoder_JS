### ABC068
[問題ページ](https://atcoder.jp/contests/abc068/tasks)

### A-ABCxxx
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    
    console.log("ABC" + N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Break Number
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    let list = [1, 2, 4, 8, 16, 32, 64];
    
    console.log(Math.max(...list.filter(n=>n<=N)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Cat Snuke and a Voyage
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const ab = arg.slice(1, M + 1);
    
    let map = [...Array(N)].fill(0);
    let answer = "IMPOSSIBLE";
    
    for(let i=0; i<M; i++) {
        let temp = ab[i].split(" ").map(n=>parseInt(n));
        let from = temp[0];
        let to   = temp[1];
        
        if(from === 1) {
            if(map[to] === 1) {
                answer = "POSSIBLE";
                break;
            } else {
                map[to]++;
            }
        }
        
        if(to === N) {
            if(map[from] === 1) {
                answer = "POSSIBLE";
                break;
            } else {
                map[from]++;
            }
        }
    }
        
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```