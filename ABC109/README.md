### ABC109
[問題ページ](https://atcoder.jp/contests/abc109/tasks)

### A-ABC333
```JavaScript
function Main(input) {
    parseInt(input);
    if( input == 7 || input == 5 || input == 3 ) {
      console.log("YES");
    } else {
      console.log("NO");
    }
}
Main(require("fs").readFileSync("/dev/stdin", "utf8"));
```

### B-Shiritori
```JavaScript
'use strict';

function main(arg) {
    const N     = parseInt(arg.split("\n")[0]);
    const words = arg.split("\n").slice(1);
    const memo  = new Set();

    let lastLetter = words[0].slice(0, 1);

    for(let i=0; i<N; i++) {
        if(lastLetter !== words[i].slice(0, 1) || memo.has(words[i])) {
            console.log('No');
            return;
        }

        lastLetter = words[i].slice(-1);
        memo.add(words[i]);
    }
    
    console.log('Yes');
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```