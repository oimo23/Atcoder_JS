### ABC047
[問題ページ](https://atcoder.jp/contests/abc047/tasks)

### A-キャンディーと2人の子供
```JavaScript
"use strict";
    
const main = arg => {
	const packs = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).sort((a,b)=>b-a);
	console.log(packs[0] === packs[1] + packs[2] ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```