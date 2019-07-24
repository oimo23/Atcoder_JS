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

### C-Sentou
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const T = parseInt(arg[0].split(" ")[1]);
    const t = arg[1].split(" ");
    
    let answer = 0;
    
    for(let i in t) {
        if(t[parseInt(i) + 1] - t[i] < T) {
            answer += t[parseInt(i) + 1] - t[i];
        } else {
            answer += T;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```