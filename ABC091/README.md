### ABC091
[問題ページ](https://atcoder.jp/contests/abc091/tasks)

### A-Two Coins
```JavaScript
"use strict";

const main = arg => {
    const coins = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    console.log(coins[0] + coins[1] >= coins[2] ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Two Colors Card Game
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const blueN = parseInt(arg[0]);
    const blueS = arg.slice(1,blueN + 1);
    const redN  = parseInt(arg[blueN + 1]);
    const redS  = arg.slice(blueN+2);

    const set = new Set(redS.concat(blueS));
    let answer = [];

    set.forEach(item => {
        let temp = 0;
        let foundInBlue = blueS.filter(n=>n==item).length;
        let foundInRed  = redS.filter(n=>n==item).length;
        
        if(foundInBlue > 0) {
            temp += foundInBlue;
        }
        
        if(foundInRed > 0) {
            temp -= foundInRed;
        }
        
        answer.push(temp);
    })
    
    console.log(Math.max(...answer) > 0 ? Math.max(...answer) : 0);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```