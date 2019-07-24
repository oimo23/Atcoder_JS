### ABC045
[問題ページ](https://atcoder.jp/contests/abc045/tasks)

### A-台形
```JavaScript
"use strict";
    
const main = arg => {
    const T = parseInt(arg.split("\n")[0]);
    const B = parseInt(arg.split("\n")[1]);
    const H = arg.split("\n")[2];
    
    console.log(((T + B) * H) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-3人でカードゲームイージー / Card Game for Three (ABC Edit)
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const A = arg[0].split("");
    const B = arg[1].split("");
    const C = arg[2].split("");
    
    let next = "a";
    
    while(true) {
        if(next === "a") {
            if(A.length === 0) {
                console.log("A");
               return;
            }
            
            next = A.shift();
        } else if(next === "b") {
            if(B.length === 0) {
                console.log("B");
                return;
            }
            
            next = B.shift();
        } else if(next === "c") {
            if(C.length === 0) {
                console.log("C");
                return;
            }
            
            next = C.shift();
        }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```