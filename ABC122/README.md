### ABC122
[問題ページ](https://atcoder.jp/contests/abc122/tasks)

### A-Double Helix
```JavaScript
"use strict";
    
const main = arg => {
    const b = arg.split("\n")[0];
    
    if(b == "A") {
        console.log("T");
    } else if (b == "T") {
        console.log("A");
    } else if (b == "C") {
        console.log("G");
    } else if (b == "G") {
        console.log("C");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ATCoder
```JavaScript
"use strict";
    
const main = arg => {
    const S = arg.split("\n")[0].split("");
    let streak = [];
    let temp = 0;
    
    for(let i in S) {
        if(S[i] == "A" || S[i] == "T" || S[i] == "C" || S[i] == "G") {
            temp++;
        } else {
            streak.push(temp);
            temp = 0;
        }
    }
    
    if(temp !== 0) {
        streak.push(temp);
    }

    console.log(Math.max(...streak));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
