### ABC060
[問題ページ](https://atcoder.jp/contests/abc060/tasks)

### A-Shiritori
```JavaScript
"use strict";
    
const main = arg => {
    const S  = arg.split("\n")[0].split(" ");
    let tail = S[0].split("").pop();

    for(let i=1; i<S.length; i++) {
        if(tail == S[i].split("")[0]) {
            tail = S[i].split("").pop();
        } else {
            console.log("NO");
            return;
        }
    }
    
    console.log("YES");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Choose Integers
```JavaScript
"use strict";
    
const main = arg => {
    const [A, B, C] = arg.split("\n")[0].split(" ");
  
    let flg = false;
    
    for(let i=0; i<B; i++) {
        if((A * i - C) % B === 0) {
            flg = true;
        }
    }
    
    console.log(flg ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```