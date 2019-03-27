### ABC071
[問題ページ](https://atcoder.jp/contests/abc071/tasks)

### A-Meal Delivery
```JavaScript
"use strict";

const main = arg => {
    const x = arg.split("\n")[0].split(" ")[0];
    const a = arg.split("\n")[0].split(" ")[1];
    const b = arg.split("\n")[0].split(" ")[2];
    console.log(Math.abs(x-a) < Math.abs(x-b) ? "A" : "B");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Not Found
```JavaScript
"use strict";
    
const main = arg => {
    const S  = arg.split("\n")[0].split("");
    const alphabets = "abcdefghijklmnopqrstuvwxyz".split("");

    for(let i in alphabets) {
        if(S.indexOf(alphabets[i]) == -1) {
            console.log(alphabets[i]);
            return;
        }
    }
    
    console.log("None");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```