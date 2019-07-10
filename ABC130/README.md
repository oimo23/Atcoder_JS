### ABC130
[問題ページ](https://atcoder.jp/contests/abc130/tasks)

### A-Ferris Wheel
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const X = parseInt(arg[0].split(" ")[0]);
    const A = parseInt(arg[0].split(" ")[1]);
    console.log(X < A ? 0 : 10);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Bounding
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const X = parseInt(arg[0].split(" ")[1]);
    
    const Ls = arg[1].split(" ").map(n=>parseInt(n));
    
    let list = [];
    
    for(let i=0; i<=N; i++) {
        if(i == 0) {
            list.push(0);
        } else {
            let temp = list[i-1] + Ls[i-1];
            list.push(temp);
        }
    
    }

    console.log(list.filter(n=>n<=X).length)
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Rectangle Cutting
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const W = parseInt(arg[0].split(" ")[0]);
    const H = parseInt(arg[0].split(" ")[1]);
    const x = parseInt(arg[0].split(" ")[2]);
    const y = parseInt(arg[0].split(" ")[3]);
    
    if(W / 2 === x && H / 2 === y) {
      console.log((W * H) / 2, 1);
    } else {
      console.log((W * H) / 2, 0);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```