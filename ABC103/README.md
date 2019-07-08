### ABC103
[問題ページ](https://atcoder.jp/contests/abc103/tasks)

### A-Task Scheduling Problem
```JavaScript
"use strict";

const main = arg => {
    arg = arg.split(" ").sort((a,b)=>a-b);
    console.log(arg[2] - arg[0]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-String Rotation
```JavaScript
"use strict";

const main = arg => {
    const origin = arg.split("\n")[0];
    let   target = arg.split("\n")[1].split("");
    
    for(let i=0; i<target.length; i++) {
        if(origin == target.join("")) {
            console.log("Yes");
            return;
        }
        
        target.unshift(target[target.length-1]);
        target.pop();
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```