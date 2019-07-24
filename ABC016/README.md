### ABC016
[問題ページ](https://atcoder.jp/contests/abc016/tasks)

### A-12月6日
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n")[0].split(" ");
    const M = parseInt(arg[0]);
    const D = parseInt(arg[1]);
    
    console.log(M % D === 0 ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-A±B Problem
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n")[0].split(" ");
    const A = ~~arg[0];
    const B = ~~arg[1];
    const C = ~~arg[2];
    
    if(A + B === C && A - B === C) {
        console.log("?");
    } else if(A + B === C) {
        console.log("+");
    } else if(A - B === C) {
        console.log("-");
    } else {
        console.log("!");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-友達の友達
```JavaScript
"use strict";

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    const graph = arg.slice(1, M + 1);
    
    const array = [...Array(N)];
    
    for(let i=0; i<N; i++) {
        array[i] = [...Array(N)].fill(1000000);
    }
    
    const warshallFloyd = (d) => {
        for(let k=0; k<N; k++) {
            for(let i=0; i<N; i++) {
                for(let j=0; j<N; j++) {
                    if(i === j) {
                        d[i][j] = 0;
                    } 
                    
                    d[i][j] = Math.min(d[i][j], d[i][k] + d[k][j]);
                }
            }
        }
        
        return d;
    }
    
    for(let i in graph) {
        let u = parseInt(graph[i].split(" ")[0]);
        let v = parseInt(graph[i].split(" ")[1]);
        
        array[u-1][v-1] = 1;
        array[v-1][u-1] = 1;
    }
    
    const d = warshallFloyd(array);
    
    for(let i=0; i<N; i++) {
        console.log(d[i].filter(n=>n==2).length);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```