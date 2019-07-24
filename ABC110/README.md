### ABC110
[問題ページ](https://atcoder.jp/contests/abc110/tasks)

### A-753
```JavaScript
"use strict";

const main = arg => {
    let temp = arg.split(" ").map(n=>parseInt(n)).sort((a,b) => b-a);
    let big  = (String(temp[0]) + String(temp[1]));

    console.log( parseInt(big) + temp[2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-754
```JavaScript
"use strict";

const main = arg => {
    const X = arg.split("\n")[0].split(" ").map(n=>parseInt(n))[2];
    const Y = arg.split("\n")[0].split(" ").map(n=>parseInt(n))[3];
    
    const x = arg.split("\n")[1].split(" ").map(n=>parseInt(n));
    const y = arg.split("\n")[2].split(" ").map(n=>parseInt(n));
    
    x.push(X);
    y.push(Y);
    
    if(Math.max(...x) < Math.min(...y)) {
        console.log("No War");
        return;
    }
    
    console.log("War");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-String Transformation
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0];
    const T = arg[1];
    
    const map1 = [...Array(26)].fill(0);
    const map2 = [...Array(26)].fill(0);
    
    for(let i=0; i<S.length; i++) {
        map1[S.charCodeAt(i) - 97]++;
        map2[T.charCodeAt(i) - 97]++;
    }
    
    map1.sort((a,b)=>a-b);
    map2.sort((a,b)=>a-b);
    
    if(map1.join("") === map2.join("")) {
        console.log("Yes");
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```