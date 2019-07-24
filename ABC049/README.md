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

### B-たてなが / Thin
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const H = arg[0].split(" ")[0];
    const W = arg[0].split(" ")[1];
    
    const pixels = arg.slice(1, H + 1);
    let answer    = [];
    
    for(let i=0; i<H; i++) {
        answer.push(pixels[i]);
        answer.push(pixels[i]);
    }
    
    console.log(answer.join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-白昼夢 / Daydream
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    
    while(S.length > 0) {
        let last5 = S.slice(-5).join("");
        let last6 = S.slice(-6).join("");
        let last7 = S.slice(-7).join("");
        
        if(last5 === "erase" || last5 === "dream") {
            S.splice(S.length - 5, 5);
        } else if(last6 === "eraser") {
            S.splice(S.length - 6, 6);
        } else if(last7 === "dreamer") {
            S.splice(S.length - 7, 7);
        } else {
            console.log("NO");
            return;
        }
    }
    
    console.log("YES");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```