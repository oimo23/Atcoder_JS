### ABC114
[問題ページ](https://atcoder.jp/contests/abc114/tasks)

### A-753
```JavaScript
"use strict";

const main = input => {
    input = parseInt(input);
    if( input == 7 || input == 5 || input == 3 ) {
      console.log("YES");
    } else {
      console.log("NO");
    }
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```

### B-754
```JavaScript
"use strict";

const main = input => {
    input = parseInt(input);
    const num = input.split("");
    
    let diff = [];
    
    for ( var i=0; i<num.length; i++) {
        var temp = num.slice(i, i+3).join("");
        diff.push(Math.abs( 753 - temp ));
    }
    
    let answer = diff.reduce((n, m) => n <= m? n: m);
    console.log(answer);
    
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

```

### C-755
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const l = String(N).length;
    
    const num = ["3", "5", "7"];
    const X   = [3, 5, 7];
    
    let answer = 0;
    let n      = 0;
    
    // まず、3,5,7から成る数字を全て列挙する
    for(let i=0; i<l-1; i++) {
        let Xl = X.length;
        for(let j=0; j<3; j++) {
            for(let k=n; k<Xl; k++) {
                X.push(parseInt(num[j] + X[k]));
            }
        }
        
        n = Xl;
    }
    
    // 3,5,7からなる数字の配列から、それぞれが1回以上登場するものに絞る
    for(let i=0; i<X.length; i++) {
        if(X[i] > N) break;
        
        let digits = String(X[i]).split("");
        
        if(digits.indexOf("3") !== -1 && digits.indexOf("5") !== -1 && digits.indexOf("7") !== -1) {
            answer++;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```