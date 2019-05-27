### ABC039
[問題ページ](https://atcoder.jp/contests/abc039/tasks)

### A-高橋直体
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    const C = arg.split("\n")[0].split(" ")[2];
    
    console.log(2 * (A * B) + 2 * (A * C) + 2 * (C * B));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-エージェント高橋君
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    
    console.log(Math.sqrt(Math.sqrt(N)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-ピアニスト高橋君
```JavaScript
"use strict";

const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    
    const eleven = S.slice(0, 11).join("");
    
    if(eleven === "WBWBWWBWBWB") {
        console.log("Do");
    }
    
    if(eleven === "WBWWBWBWBWW") {
        console.log("Re");
    }
    
    if(eleven === "WWBWBWBWWBW") {
        console.log("Mi");
    }
    
    if(eleven === "WBWBWBWWBWB") {
        console.log("Fa");
    }
    
    if(eleven === "WBWBWWBWBWW") {
        console.log("So");
    }
    
    if(eleven === "WBWWBWBWWBW") {
        console.log("La");
    }
    
    if(eleven === "WWBWBWWBWBW") {
        console.log("Si");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```