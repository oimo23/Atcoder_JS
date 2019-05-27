### ABC004
[問題ページ](https://atcoder.jp/contests/abc004/tasks)

### A-流行
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = arg[0].split(" ");
    
    console.log(2 * N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-回転
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const table = arg.map(n=>n.split(""));
    
    let answer = [];
    
    for(let i in table) {
        answer.push(table[table.length - 1 - i].reverse());
    }
    
    console.log(answer.map(n=>n.join("")).join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-入れ替え
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0] % 30;
    const cards = [1, 2, 3, 4, 5, 6];
    
    for(let i=0; i<N; i++) {
        let mod = i % 5;
        cards[mod] = [cards[mod + 1], cards[mod + 1] = cards[mod]][0];
    }
    
    console.log(cards.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
