### ABC049
[問題ページ](https://atcoder.jp/contests/abc049/tasks)

### A-居合を終え、青い絵を覆う
```JavaScript
"use strict";
    
const main = arg => {
    const c = arg.split("\n")[0];
    const vowels = ["a", "i", "u", "e", "o"];
    
    console.log(vowels.filter(n=>n==c).length ? "vowel" : "consonant");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```