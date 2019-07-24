### ABC005
[問題ページ](https://atcoder.jp/contests/abc005/tasks)

### A-おいしいたこ焼きの作り方
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const x = arg[0].split(" ")[0];
    const y = arg[0].split(" ")[1];
    
    console.log(Math.floor(y / x));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-おいしいたこ焼きの食べ方
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0];
    const T = arg.slice(1, N + 1).map(n=>~~n);
    
    console.log(Math.min(...T));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-おいしいたこ焼きの売り方
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const T = parseInt(arg[0]);
    const N = parseInt(arg[1]);
    const times = arg[2].split(" ").map(n=>parseInt(n));
    
    const M = parseInt(arg[3]);
    const customers = arg[4].split(" ").map(n=>parseInt(n));
    
    for(let i in customers) {
        let eatTako = times.filter(time=>customers[i] - time <= T && customers[i] - time >= 0)[0];
        
        if(!eatTako) {
            console.log("no");
            return;
        }
        
        times.splice(times.indexOf(eatTako), 1);
    }
    
    console.log("yes");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```