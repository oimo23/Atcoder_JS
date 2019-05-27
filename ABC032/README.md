### ABC032
[問題ページ](https://atcoder.jp/contests/abc032/tasks)

### A-高橋君と青木君の好きな数
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0]);
    const B = parseInt(arg.split("\n")[1]);
    const N = parseInt(arg.split("\n")[2]);
    
    let i = N;
    
    while(true) {
        if(i % A === 0 && i % B === 0) {
            console.log(i);
            return;
        }
        i++;
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-高橋君とパスワード
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0];
    const K = ~~arg[1];
    
    let list = [];
    
    for(let i=0; i<=S.length - K; i++) {
        list.push(S.slice(i, ~~i + K));
    }
    
    let set = new Set(list);
    
    console.log(set.size);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-列
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const S = [];
    let hasZero = false;
    
    for(let i=1; i<N+1; i++){
        S[i] = parseInt(arg[i]);
        
        if(S[i] === 0) {
            hasZero = true;
        }
    }
    
    if(hasZero){
        console.log(N);
        return;
    }
    
    let start  = 0
    let end    = 0;
    let total  = 1;
    let answer = 0;
    
    // 尺取法
    for(let start=0; start<N; start++){
        if(start >= end){
            end = start;
            total = 1;
        }
        
        // 左端が右端を追い越していない &&  区間の積がK以下である
        while(start <= end && total * S[end] <= K){
            // これまでの答えと比較して、さらに長ければ答えを更新
            answer = Math.max(answer, end - start + 1);

            total *= S[end++];
        }
        
        // 現在の左端で割ることで、左端を除外出来る
        total /= S[start];
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
