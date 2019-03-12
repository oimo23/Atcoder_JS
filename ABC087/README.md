### ABC087
[問題ページ](https://atcoder.jp/contests/abc087/tasks)

### A-Buying Sweets
```JavaScript
"use strice";

function main(arg) {
    const price   = parseInt(arg.split("\n")[0]);
    const cake    = parseInt(arg.split("\n")[1]);
    const donut   = parseInt(arg.split("\n")[2]);
    console.log((price - cake) % donut);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```