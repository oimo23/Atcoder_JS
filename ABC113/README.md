### ABC113
[問題ページ](https://atcoder.jp/contests/abc113/tasks)

### A-Discount Fare
```JavaScript
const main = arg => {
    const fares = arg.split(" ").map(n => parseInt(n));
    console.log(fares[0] + (fares[1] / 2))
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Palace
```JavaScript
"use strict";

const main = arg => {
    const tmp = arg.split("\n");
    const N = parseInt(tmp[0]);
    const T = parseInt(tmp[1].split(" ")[0]);
    const A = parseInt(tmp[1].split(" ")[1]);
    const H = tmp[2].split(" ").map(n=>parseInt(n));
    let diffs = [];
    
    for(let i=0; i<H.length; i++) {
        const H_ave = T - (H[i] * 0.006);
        diffs.push(Math.abs(A - H_ave));
    }
    
    const minDiff = Math.min(...diffs);
    let answer = diffs.indexOf(minDiff);
    
    console.log(answer + 1);
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-ID
```JavaScript
"use strict";
    
const make6digit = num => {
    num = String(num);
    let digit = num.split("").length;
    
    if(digit < 6) {
        for(let i=0; i<6-digit; i++) {
            num = "0" + num;
        }
    }
    
    return num;
}

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const cities = arg.slice(1, M + 1);
    let data = [];
    
    for(let i in cities) {
        let tempPrefecture = parseInt(cities[i].split(" ")[0]);
        let tempBirth      = parseInt(cities[i].split(" ")[1]);
        
        data.push({
            prefecture: tempPrefecture,
            birth:      tempBirth,
            index:      i
        })
    }
    
    data.sort((a,b) => {
        if(a.prefecture < b.prefecture) {
            return -1;
        }
        
        if(a.prefecture > b.prefecture) {
            return 1;
        }
        
        if(a.birth < b.birth) {
            return -1;
        }
        
        if(a.birth > b.birth) {
            return 1;
        }
    });
    
    let num = 1;
    
    for(let i in data) {
        if(data[i-1]) {
            if(data[i].prefecture !== data[i-1].prefecture) {
                num = 1;
            }
        }
        
        let firstHalf = make6digit(data[i].prefecture);
        let lastHalf  = make6digit(num);
        
        const id = firstHalf + lastHalf;
        
        data[i].id = id;
        
        num++;
    }
    
    data.sort((a,b)=>a.index - b.index);
    
    for(let i in data) {
        console.log(data[i].id);   
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```