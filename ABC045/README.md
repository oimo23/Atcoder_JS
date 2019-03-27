### ABC045
[問題ページ](https://atcoder.jp/contests/abc045/tasks)

### A-台形
```JavaScript
"use strict";
    
const main = arg => {
    const T = parseInt(arg.split("\n")[0]);
    const B = parseInt(arg.split("\n")[1]);
    const H = arg.split("\n")[2];
    
    console.log(((T + B) * H) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```