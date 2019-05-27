### ABC041
[問題ページ](https://atcoder.jp/contests/abc041/tasks)

### A-添字
```JavaScript
'use strict';

function main(arg) {
    console.log(arg.split(" ")[0] % arg.split(" ")[1] === 0 ? 0 : 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-背の順
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ");
    
    const heightAndNumber = [];
    
    for(let i in a) {
        let temp = {num: parseInt(i) + 1, height: a[i]};
        heightAndNumber.push(temp);
    }
    
    heightAndNumber.sort((a,b)=>b.height - a.height);
    
    for(let i in heightAndNumber) {
        console.log(heightAndNumber[i].num);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
