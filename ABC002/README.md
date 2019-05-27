### ABC002
[問題ページ](https://atcoder.jp/contests/abc002/tasks)

### A-正直者
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const numbers = arg[0].split(" ");
    
    console.log(Math.max(...numbers));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-罠
```JavaScript
"use strict";

const main = arg => {
    const S = arg.split("\n")[0].split("");
    const vowels = ["a", "i", "u", "e", "o"];
    
    for(let i in S) {
        for(let j=0; j<vowels.length; j++) {
            if(S[i] === vowels[j]) {
                S[i] = "";
            }
        }   
    }
        
    console.log(S.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```