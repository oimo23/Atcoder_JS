### ABC133
[問題ページ](https://atcoder.jp/contests/abc133/tasks)

### A-T or T
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const A = parseInt(arg[0].split(" ")[1]);
    const B = parseInt(arg[0].split(" ")[2]);
    
    const train = N * A;
    const bus  = B;
    
    console.log(Math.min(train, bus));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Good Distance
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const D = parseInt(arg[0].split(" ")[1]);
    
    const points = arg.slice(1, N + 1);
    let answer = 0;
    
    for(let i in points) {
        let temp = points[i].split(" ").map(n=>parseInt(n));
        let nows = [];
        
        for(let j in temp) {
            nows.push(temp[j]);           
        }
        
        for(let j=parseInt(i)+1; j<N; j++) {
            let temp = points[j].split(" ").map(n=>parseInt(n));
            let targets = [];
            
            for(let k in temp) {
                targets.push(temp[k]);           
            }
            
            let distance = 0;
            
            for(let k in targets) {
                distance += Math.abs(Math.pow(nows[k] - targets[k], 2));
            }
            
            distance = Math.sqrt(distance);
            
            if(distance % 1 === 0) {
                answer++
            }
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Remainder Minimization 2019
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const L = parseInt(arg[0].split(" ")[0]);
    const R = parseInt(arg[0].split(" ")[1]);
    
    if(R - L + 1 >= 2019) {
        // 2つの数の差が2019以上のとき、必ず2019の倍数が存在するので0
        console.log(0);
    } else {
        const Lmod = L % 2019;
        const Rmod = R % 2019;
        
        let min = Infinity;
        
        for(let i=Lmod; i<Rmod; i++) {
            for(let k=parseInt(i)+1; k<=Rmod; k++) {
                min = Math.min((i * k) % 2019, min);
            }
        }
        
        console.log(min);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```