### ABC110
[問題ページ](https://atcoder.jp/contests/abc110/tasks)

### A-753
```JavaScript
'use strict';

function main(arg) {
    let temp = arg.split(" ").map(n=>parseInt(n)).sort((a,b) => b-a);
    let big  = (String(temp[0]) + String(temp[1]));

    console.log( parseInt(big) + temp[2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-754
```JavaScript
'use strict';

function main(arg) {
    let X = arg.split("\n")[0].split(" ").map(n=>parseInt(n))[2];
    let Y = arg.split("\n")[0].split(" ").map(n=>parseInt(n))[3];
    
    let x = arg.split("\n")[1].split(" ").map(n=>parseInt(n));
    let y = arg.split("\n")[2].split(" ").map(n=>parseInt(n));
    
    x.push(X);
    y.push(Y);
    
    if(Math.max(...x) < Math.min(...y)) {
            console.log("No War");
            return;
    }
    
    console.log("War")
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```