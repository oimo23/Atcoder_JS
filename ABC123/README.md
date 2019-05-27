### ABC123
[問題ページ](https://atcoder.jp/contests/abc123/tasks)

### A-Five Antennas
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");

    const k = parseInt(arg.slice(5, arg.length));
    const antennas = arg.slice(0, arg.length - 1).map(n=>parseInt(n));
    
    console.log(antennas[4] - antennas[0] > k ? ":(" : "Yay!");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Five Dishes
```JavaScript
"use strict";
    
const main = arg => {
    const times = arg.split("\n").map(n=>parseInt(n));
    let min = 10;
    let sum = 0;
    
    for(let i=0; i<5; i++) {
        let digitOne = times[i] % 10;
        sum += parseInt(times[i]);
        
        if(10 - digitOne !== 10) {
            sum += 10 - digitOne;
        }
        
        if(10 - digitOne !== 10 && digitOne < min) {
            min = digitOne;
        }
    }

    console.log(parseInt(sum - (10 - min)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
