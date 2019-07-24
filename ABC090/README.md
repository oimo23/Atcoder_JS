### ABC090
[問題ページ](https://atcoder.jp/contests/abc090/tasks)

### A-Diagonal String
```JavaScript
"use strict";

const main = arg => {
    const letters = arg.split("\n").map(n=>n.split(""));
    console.log(letters[0][0] + letters[1][1] + letters[2][2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Palindromic Numbers
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    let cnt = 0;
    
    for(let i=A; i<=B; i++) {
        if(String(i) == String(i).split("").reverse().join("")) {
            cnt++;
        }
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Flip,Flip, and Flip......
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    let answer = 0;
    
    if(N === 1 && M === 1) {
        answer = 1;
    } else if(N === 1) {
        answer = M - 2;
    } else if(M === 1) {
        answer = N - 2;
    } else {
        answer = (N - 2) * (M - 2);
    }
    
    // 桁溢れ対策  original (id: macco さん)
    if (answer > Number.MAX_SAFE_INTEGER) {

    const multi_biggerInt = (a, b) => {
      const num1 = String(a).split('').map(n => Number(n)).reverse();
      const num2 = String(b).split('').map(n => Number(n)).reverse();

      let ans = [...Array(num1.length + num2.length)].fill(0);

      const checkCarry = () => {
        for (let i = 0; i < ans.length; i++) {
          if (ans[i] >= 10) {
            const upper = Number(String(ans[i]).split('')[0]);
            const lower = Number(String(ans[i]).split('')[1]);

            ans[i - 1] += upper;
            ans[i] = lower;
          }
        }
      }

      for (let i = 0; i < num1.length; i++) {
        for (let j = 0; j < num2.length; j++) {
          const pro   = num1[i] * num2[j];
          const digit = ans.length - (i + j) - 1;

          ans[digit] += pro;
          checkCarry();
        }
      }

      for (let i = 0; i < ans.length; i++) {
        if (ans[i] !== 0) {
          ans = ans.slice(i);
          break;
        }
      }

      return ans.join('');
      }

      answer = multi_biggerInt(Math.abs(N - 2), Math.abs(M - 2));
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```