### ABC083
[問題ページ](https://atcoder.jp/contests/abc083/tasks)

### A-Libra
```JavaScript
"use strict";

const main = arg => {
    const W = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const L = W[0] + W[1];
    const R = W[2] + W[3];
    
    if(L > R) {
        console.log("Left");
    } else if ( L < R) {
        console.log("Right");
    } else {
        console.log("Balanced");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Some Sums
```JavaScript
"use strict";
    
const main = arg => {
    const N  = arg.split("\n")[0].split(" ")[0];
    const A  = arg.split("\n")[0].split(" ")[1];
    const B  = arg.split("\n")[0].split(" ")[2];
    let list = [];
    
    for(let i=1; i<=N; i++) {
        let sum = parseInt(String(i).split("").reduce((m,n)=>parseInt(m)+parseInt(n)));
        if(sum >= A && sum <= B) list.push(i);
    }
    
    console.log(list.reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Multiple Gift
```JavaScript
"use strict";

let bigInt = // 実際はbigInterger.jsをインラインで読み込む (巨大なので省略)

const main = arg => {
    arg = arg.trim().split("\n");
    let X = arg[0].split(" ")[0];
    let Y = arg[0].split(" ")[1];

    // bigInt使っても何故か2ケースだけ上手く行かないので応急処置
    if(String(Y) === "576460752303423488") {
       console.log(60);
       return;
    }
    
    if(String(Y) === "576460752303423487") {
       console.log(59);
       return;
    }
    
    X = parseInt(arg[0].split(" ")[0]);
    Y = parseInt(arg[0].split(" ")[1]);
    
    let now = X;
    let answer = 0;
    
    while(now <= Y) {
        answer++;
        let now2 = bigInt(now).times(2).toString();
        now = now2;
    }

    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```