### ABC043
[問題ページ](https://atcoder.jp/contests/abc043/tasks)

### A-キャンディーとN人の子供イージー
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    
    console.log((N * (N + 1)) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-バイナリハックイージー / Unhappy Hacking (ABC Edit)
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const s = arg[0];
    
    let answer = [];
    
    for(let i=0; i<s.length; i++) {
        if(s[i] === "0") {
            answer.push(0);
        }
        
        if(s[i] === "1") {
            answer.push(1);
        }
        
        if(s[i] === "B" && answer.length > 0) {
            answer.pop();
        }
    }
    
    console.log(answer.join(""));
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-いっしょ / Be Together
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const a = arg[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    let list = [];

    for(let i=a[0]; i<a[a.length - 1]; i++) {
        let temp = 0;
        
        for(let j in a) {
            temp += Math.pow(a[j] - i, 2);
        }
        
        list.push(temp);
    }
    
    if(list.length) {
        console.log(Math.min(...list));
    } else {
        console.log(0);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```