### ABC046
[問題ページ](https://atcoder.jp/contests/abc046/tasks)

### A-AtCoDeerくんとペンキ
```JavaScript
"use strict";
    
const main = arg => {
    const colors = arg.split("\n")[0].split(" ");
    const set = new Set(colors);
    
    console.log(set.size);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```