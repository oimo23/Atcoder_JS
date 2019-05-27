### ABC119
[問題ページ](https://atcoder.jp/contests/abc119/tasks)

### A-Still TBD
```JavaScript
"use strict";

function main(arg) {
    const S = arg.split("\n")[0].split("/");
    let answer;
    
    if(parseInt(S[0]) < 2019) {
        answer = "TBD";
    } else if (parseInt(S[0]) == 2019 && parseInt(S[1]) > 4) {
        answer = "TBD";
    } else {
        answer = "Heisei";
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Digital Gifts
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    const X = arg.split("\n").slice(1,N+1);
    let total = 0;

    for(let i in X) {
        let money;
        if(X[i].split(" ")[1] == "BTC") {
            money = X[i].split(" ")[0] * 380000.0;
        } else {
            money = X[i].split(" ")[0];
        }
        total += Number(money);
    }
    
    console.log(total);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
