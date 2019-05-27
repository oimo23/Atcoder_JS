### ABC017
[問題ページ](https://atcoder.jp/contests/abc017/tasks)

### A-プロコン
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const scores = arg.map(n=>n.split(" ").map(m=>parseInt(m)));
    let answer   = 0;
    
    for(let i in scores) {
        answer += scores[i][0] * (scores[i][1] / 10);
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-choku語
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("ch").join("C").split("");
    
    const set = new Set(S);
    const uniqueS = [...set];
    
    for(let i in uniqueS) {
        if(
            uniqueS[i] !== "C"  &&
            uniqueS[i] !== "o"  && 
            uniqueS[i] !== "u"  &&
            uniqueS[i] !== "k"
        ) {
            console.log("NO");
            return;
        }
    }
    
    console.log("YES");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```