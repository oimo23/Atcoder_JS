### ABC111
[問題ページ](https://atcoder.jp/contests/abc111/tasks)

### A-AtCoder Beginner Contest 999
```JavaScript
"use strict";

const convertOneNine = target => {
    if(target == 1) return 9;
    if(target == 9) return 1;
}

const main = arg => {
    let answer = String(arg).split("").map(n=>convertOneNine(parseInt(n)));
    console.log(answer.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AtCoder Beginner Contest 111
```JavaScript
"use strict";

const main = arg => {
    const N = String(arg).split("").map(n=>parseInt(n));
    let answer;


    if(N[1] <= N[0] && N[2] <= N[0]) {
        answer = String(N[0]) + String(N[0]) + String(N[0]);
        console.log(answer);
    } else {
        answer =  String(N[0]+1) + String(N[0]+1) + String(N[0]+1);
        console.log(answer);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-/\/\/\/
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    
    const N    = ~~arg[0].split(" ")[0];
    const v    = arg[1].split(" ").map(n=>~~n);
    
    let even = [];
    let odd  = [];
    
    for(let i=0; i<N; i++) {
        const h = v[i];
        let a = (i % 2 ? odd : even)[h];
        
        a = a || {val:h, count: 0};
        a.count++;
        
        if(i % 2) {
            odd[h] = a;
        } else {
            even[h] = a;
        }
    }
    
    even = even.sort((a,b)=>a.count-b.count).reverse().filter(a=>a);
    odd  = odd.sort((a,b)=>a.count-b.count).reverse().filter(a=>a);
  
    if(even[0].val!=odd[0].val){
        console.log(N - even[0].count - odd[0].count);
        return;
    }
    
    // 全て同じ値のとき
    if(!even[1] && !even[2]){
        console.log(N/2);
        return;
    }
    
    // 偶数番目のみ全て同じ値のとき
    if(!even[1]){
        console.log(N - even[0].count - odd[1].count);
        return;
    }
    
    // 奇数番目のみ全て同じ値のとき
    if(!odd[1]){
        console.log(N - even[1].count - odd[0].count);
        return;
    }
    
    console.log(Math.min(
        N - even[0].count - odd[1].count,
        N - even[1].count - odd[0].count
    ));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```