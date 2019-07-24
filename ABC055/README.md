### ABC055
[問題ページ](https://atcoder.jp/contests/abc055/tasks)

### A-Restaurant
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0].split(" ")[0]);
    
    console.log((800*N) - (Math.floor(N/15)*200));

}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Training Camp
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0];
    
    let answer = 1;
    
    for(let i=2; i<=N; i++) {
        answer *= i;
        answer %= Math.pow(10, 9) + 7;
    }

    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Scc Puzzle
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    let S = parseInt(arg[0].split(" ")[0]);
    let C = Math.floor(parseInt(arg[0].split(" ")[1]) / 2);
    
    let cnt = 0;
    
    if(S > C) {
        console.log(C);
    } else {
        C -= S;
        console.log(S + Math.floor(C / 2))
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```