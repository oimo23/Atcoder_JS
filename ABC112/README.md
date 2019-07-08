### ABC112
[問題ページ](https://atcoder.jp/contests/abc112/tasks)

### A-Programming Education
```JavaScript
"use strict";

const main = arg => {
   const age = arg.split("\n")[0];
   const A   = parseInt(arg.split("\n")[1]);
   const B   = parseInt(arg.split("\n")[2]);
   
   if(age == 2) {
       console.log(A + B);
   } else {
       console.log("Hello World");
   }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Time Limit Exceeded
```JavaScript
"use strict";
 
const main = input => {
    input = input.split("\n");
    const T = Number(input[0].split(" ")[1]);
    input.shift();
    let min = 9999;
  
    for (let i = 0; i < input.length; i++) {
        let tmp = input[i].split(" ").map(n => Number(n));
        if (tmp[1] <= T && tmp[0] < min) {
            min = tmp[0];
        }
    }
  
    console.log(min == 9999 ? "TLE" : min);
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```