### ABC077
[問題ページ](https://atcoder.jp/contests/abc077/tasks)

### A-Rotation
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0];
    const B = arg.split("\n")[1];
    
    console.log(B.split("").reverse().join("") == A ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Around Square
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    
    if(N === 1 || N === 2) {
        console.log(1);
        return;
    }
    
    for(let i=1; i<N; i++) {
        if(Math.pow(i, 2) > N) {
            console.log(Math.pow(i-1, 2));
            return;
        }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Snuke Festival
```JavaScript
"use strict";
    
const lower_bound = (array, target) => {
    var min = 0;
    var max = array.length - 1;
    while (min <= max) {
        var middle = min + Math.floor((max - min) / 2);
        if (array[middle] < target) {
            min = middle + 1;
        }
        else {
            max = middle - 1;
        }
    }
 
    return min;
}
 
const upper_bound = (array, target) => {
    var min = 0;
    var max = array.length - 1;
    while (min <= max) {
        var middle = min + Math.floor((max - min) / 2);
        if (array[middle] <= target) {
            min = middle + 1;
        }
        else {
            max = middle - 1;
        }
    }
 
    return min;
}

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const top = arg[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    const mid = arg[2].split(" ").map(n=>parseInt(n));
    const low = arg[3].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    let cnt = 0;
    
    for(let i in mid) {
        let topNum = lower_bound(top, mid[i]);
        let lowNum = low.length - upper_bound(low, mid[i]);

        cnt += topNum * lowNum;
    }
    
    console.log(cnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```