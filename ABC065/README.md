### ABC065
[問題ページ](https://atcoder.jp/contests/abc065/tasks)

### A-Expired?
```JavaScript
"use strict";

const main = arg => {
    const X = parseInt(arg.split("\n")[0].split(" ")[0]);
    const A = parseInt(arg.split("\n")[0].split(" ")[1]);
    const B = parseInt(arg.split("\n")[0].split(" ")[2]);
    
    if((B - A) >= X + 1) {
        console.log("dangerous");
    } else if((B - A) <= X && (B - A) > 0) {
        console.log("safe");
    } else {
        console.log("delicious");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Reconciled?
```JavaScript
"use strict";


const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    // 差が2以上あると交互に並べられない
    if(Math.abs(N - M) > 1) {
        console.log(0);
        return;
    }
    
    const MOD = 1e9 + 7;
    let answer = 1;
    
    for(let i=1; i<=N; i++) {
        answer = (answer % MOD) * (i % MOD);
    }
    
    for(let i=1; i<=M; i++) {
        answer = (answer % MOD) * (i % MOD);
    }
    
    /* -----------------------------------------------------
       差が0のときは、組み合わせが2通り 例：犬猿犬猿, 猿犬猿犬
       差が1のときは、組み合わせが1通り 例：犬猿犬猿犬
       それによって答えを2倍にするかどうか分ける
    --------------------------------------------------------*/
    console.log(answer * ((N == M) + 1) % MOD);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```