### ABC078
[問題ページ](https://atcoder.jp/contests/abc078/tasks)

### A-HEX
```JavaScript
"use strict";
    
const main = arg => {
    const X = arg.split("\n")[0].split(" ")[0];
    const Y = arg.split("\n")[0].split(" ")[1];
    
    if(X == Y) {
        console.log("=");
        return;
    }
    
    if(X < Y) {
        console.log("<");
        return;
    }
    
    if(X > Y) {
        console.log(">");
        return;
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-ISU
```JavaScript
"use strict";
    
const main = arg => {
    const X = parseInt(arg.split("\n")[0].split(" ")[0]);
    const Y = parseInt(arg.split("\n")[0].split(" ")[1]);
    const Z = parseInt(arg.split("\n")[0].split(" ")[2]);
    
    console.log(Math.floor((X-Z)/(Y+Z)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```