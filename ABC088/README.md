### ABC088
[問題ページ](https://atcoder.jp/contests/abc088/tasks)

### A-Infinite Coins
```JavaScript
"use strict";

const main = arg => {
    const price   = parseInt(arg.split("\n")[0]);
    const dama1   = parseInt(arg.split("\n")[1]);
    console.log(price % 500 <= dama1 ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Card Game for Two
```JavaScript
"use strict";
    
const main = arg => {
    const N     = arg.split("\n")[0];
    const cards = arg.split("\n")[1].split(" ").sort((a,b)=>b-a).map(n=>parseInt(n));
    let alice = 0;
    let bob = 0;
    
    for(let i in cards) {
        if(i % 2 === 0) {
            alice += cards[i];
        } else {
            bob += cards[i];
        }
    }
    console.log(alice - bob);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```