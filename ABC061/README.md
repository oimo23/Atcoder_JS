### ABC061
[問題ページ](https://atcoder.jp/contests/abc061/tasks)

### A-Between Two Integers
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    const C = parseInt(arg.split("\n")[0].split(" ")[2]);
    console.log(A <= C && C <= B ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Counting Roads
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    const M = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    const path = arg.split("\n").slice(1, M + 1);
    const map = new Array(N).fill(0);
    path.forEach(v => {
        let a = parseInt(v.split(' ')[0]) - 1;
        let b = parseInt(v.split(' ')[1]) - 1;
        map[a]++;
        map[b]++;
    })
    map.forEach(v => console.log(v));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Big Array
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    const numbers = arg.slice(1, N+1);
    
    const map = [];
    
    for(let i in numbers) {
        let temp = numbers[i].split(" ").map(n=>parseInt(n));
        
        let number = temp[0];
        let amount = temp[1];
        
        map.push({number: number, amount: amount})
    }
    
    map.sort((a,b)=>a.number - b.number);
    
    let sum = 0;
    let i   = 0;
    
    while(sum < K) {
        sum += map[i].amount;
        i++;
    }
    
    console.log(map[i - 1].number);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```