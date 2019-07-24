### ABC064
[問題ページ](https://atcoder.jp/contests/abc064/tasks)

### A-RGB Cards
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ").join("");
    
    console.log(N % 4 === 0 ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Traveling AtCoDeer Problem
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    console.log(Math.max(...a) - Math.min(...a));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Colorful Leaderboard
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ").map(n=>parseInt(n));
    let free = 0;
    
    const map = {
        grey:   false,
        brown:  false,
        green:  false,
        mizu:   false,
        blue:   false,
        yellow: false,
        orange: false,
        red:    false
    }
    
    for(let i in a) {
        if(a[i] < 400) {
            map.grey = true;
        } else if(a[i] < 800) {
            map.brown = true;
        } else if(a[i] < 1200) {
            map.green = true;
        } else if(a[i] < 1600) {
            map.mizu = true;
        } else if(a[i] < 2000) {
            map.blue = true;
        } else if(a[i] < 2400) {
            map.yellow = true;
        } else if(a[i] < 2800) {
            map.orange = true;
        } else if(a[i] < 3200) {
            map.red = true;
        } else {
            free++;
        }
    }
    
    const existColorsNum = Object.keys(map).filter(key=>map[key] === true).length;
    
    const min = existColorsNum === 0 ? 1 : existColorsNum;
    const max = existColorsNum + free;
    
    console.log(min + " " + max);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```