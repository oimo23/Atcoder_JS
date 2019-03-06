### ABC097
[問題ページ](https://atcoder.jp/contests/abc097/tasks)

### A-Colorful Transceivers
```JavaScript
"use strict";

function main(arg) {
    const positions = arg.split("\n")[0].split(" ").slice(0,3);
    const limit     = arg.split("\n")[0].split(" ")[3];

    
    if(Math.abs(positions[2] - positions[0]) <= limit) {
        console.log("Yes");
        return;
    }
    
    if( (Math.abs(positions[1] - positions[0]) <= limit) &&
        (Math.abs(positions[2] - positions[1]) <= limit) ) {
        console.log("Yes");
        return;
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Exponential
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    const powerOf = [1]; 
    
    for(let i=2; i<=32; i++) {
        let pow = 2;
        while(Math.pow(i, pow) <= N) {
            powerOf.push(Math.pow(i,pow));
            pow++;
        }
    }
    
    console.log(Math.max(...powerOf));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```