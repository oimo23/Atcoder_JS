### ABC072
[問題ページ](https://atcoder.jp/contests/abc072/tasks)

### A-Sandglass2
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ")[0];
    const t = arg.split("\n")[0].split(" ")[1];
    console.log(N - t > 0 ? N - t : 0);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-OddString
```JavaScript
"use strict";
    
const main = arg => {
    const S  = arg.split("\n")[0].split("");
    let answer = [];
    
    for(let i in S) {
        if(i % 2 === 0) answer.push(S[i]);
    }
    
    console.log(answer.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Together
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ").map(n=>parseInt(n));
    
    const mapArray = [...Array(100000)].fill(0);
    
    for(let val of a) {
        mapArray[val]++;
        if(val > 0)     mapArray[val-1]++;
        if(val < 99999) mapArray[~~val+1]++;
    }
    
    console.log(Math.max(...mapArray));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```