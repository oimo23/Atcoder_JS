### ABC001
[問題ページ](https://atcoder.jp/contests/abc001/tasks)

### A-積雪深差
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = parseInt(arg[0].split(" ")[0]);
    const B = parseInt(arg[0].split(" ")[1]);
    
    if(A >= 13) {
        console.log(B);
    } else if(13 > A && A >= 6) {
        console.log(B / 2);
    } else {
        console.log(0);
    }
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-視程の通報
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const r = parseInt(arg[0].split(" ")[0]);
    const D = parseInt(arg[0].split(" ")[1]);
    let X = parseInt(arg[0].split(" ")[2]);
    
    for(let i=0; i<10; i++) {
        let temp = (r * X) - D;
        console.log(temp);
        
        X = temp;
    }
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
