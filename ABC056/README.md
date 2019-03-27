### ABC056
[問題ページ](https://atcoder.jp/contests/abc056/tasks)

### A-HonestOrDishonest
```JavaScript
"use strict";
    
const main = arg => {
    const a = arg.split("\n")[0].split(" ")[0];
    const b = arg.split("\n")[0].split(" ")[1];
    
    if(a=="D") {
        console.log(b == "H" ? "D" : "H");   
    } else {
        console.log(b);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-NarrowRectanglesEasy
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const W = parseInt(arg[0].split(" ")[0]);
    const a = parseInt(arg[0].split(" ")[1]);
    const b = parseInt(arg[0].split(" ")[2]);
    
    if(a <= b && b <= (a + W)) {
        console.log(0);
        return;
    }
    
    if(a <= (b + W) && (b + W) <= (a + W)) {
        console.log(0);
        return;
    }
    
    console.log(a < b ? b - (a + W) : a - (b + W));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```