### ABC022
[問題ページ](https://atcoder.jp/contests/abc022/tasks)

### A-Best Body
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N    = arg[0].split(" ")[0];
    const low  = arg[0].split(" ")[1];
    const high = arg[0].split(" ")[2];
    
    let weight    = parseInt(arg[1]);
    const changes = arg.slice(1, N + 1).map(n=>parseInt(n)); 
    let answer    = 0;
    
    for(let i in changes) {
        if(i !== "0") {
            weight += changes[i];
        }

        if(low <= weight &&  weight <= high) {
            answer++;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Bumble Bee
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const A = arg.slice(1, N + 1).map(n=>~~n);
    
    const set = new Set(A);
    
    console.log(A.length - set.size);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```