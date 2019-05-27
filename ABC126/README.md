### ABC126
[問題ページ](https://atcoder.jp/contests/abc126/tasks)

### A-Changing a Character
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const S = arg[1].split("");
    
    for(let i in S) {
        if(~~i + 1 === K) {
            S[i] = S[i].toLowerCase();
        }
    }
    
    console.log(S.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-YYMM or MMYY
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split(" ")[0];
    
    const first = S.slice(0, 2);
    const last  = S.slice(2, 4);

    // 両方1~12
    if(
        (parseInt(first) > 0 && 12 >= parseInt(first)) &&
        (parseInt(last) > 0  && 12 >= parseInt(last))
    ) {
        console.log("AMBIGUOUS");
        return;
    }
    
    // YYMMだけ有りえる場合
    if(
        (parseInt(first) <= 0 || 12 < parseInt(first)) &&
        (parseInt(last) > 0  && 12 >= parseInt(last))
    ) {
        console.log("YYMM");
        return;
    }
    
    // MMYYだけ有りえる場合
    if(
        (parseInt(first) > 0 && 12 >= parseInt(first)) &&
        (parseInt(last) <= 0 || 12 < parseInt(last))
    ) {
        console.log("MMYY");
        return;
    }

    console.log("NA");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Dice and Coin
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    let answer = 0;
    
    for(let i=1; i<=N; i++) {
        let temp;
        let x = 1 / N;
        
        if(i >= K) {
            answer += x * 1;
        } else {
            let j = 0;
            
            while(i * Math.pow(2, j) < K) {
                j++;
            }
            
            let y = Math.pow((1 / 2), j);
            answer += x * y;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```