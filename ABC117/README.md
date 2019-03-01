### ABC117
[問題ページ](https://atcoder.jp/contests/abc117/tasks)

### A-Entrance Examination
```JavaScript
function main(arg) {
    console.log(arg.split(" ")[0] / arg.split(" ")[1]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Polygon
```JavaScript
'use strict';

function main(arg) {
    let N = arg.split("\n")[0];
    let L = arg.split("\n")[1].split(" ").map(n=>parseInt(n));
    
    let max    = Math.max(...L);
    let others = L.reduce((m,n)=>m+n) - max;
    
    console.log(max < others ? 'Yes' : 'No');
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```