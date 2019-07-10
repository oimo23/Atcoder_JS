### ABC128
[問題ページ](https://atcoder.jp/contests/abc128/tasks)

### A-Apple Pie
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = parseInt(arg[0].split(" ")[0]);
    const P = parseInt(arg[0].split(" ")[1]);
    
    console.log(Math.floor(((A * 3) + P) / 2));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Guidebook
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0]);
    const AP = arg.slice(1, N + 1);
    
    const shop = [];
    
    for(let i in AP) {
        let n  = AP[i].split(" ")[0];
        let s  = parseInt(AP[i].split(" ")[1]);

        const temp = {name: n, score: s, originIdx: parseInt(i)};
        shop.push(temp);
    }
    
    shop.sort((a,b)=>{
        if(a.name < b.name) {
            return -1;
        }
        
        if(a.name > b.name) {
            return 1;
        }
        
        if(a.score > b.score) {
            return -1;
        }
        
        if(a.score < b.score) {
            return 1;
        }
        
        return 0;
    });

    for(let i in shop) {
        console.log(shop[i].originIdx + 1);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Switches
```JavaScript
"use strict";
    
const permutateWithRepetitions = (
  permutationOptions,
  permutationLength
) => {
  if (permutationLength === 1) {
    return permutationOptions.map(permutationOption => [permutationOption]);
  }

  const permutations = [];

  const smallerPermutations = permutateWithRepetitions(
    permutationOptions,
    permutationLength - 1
  );

  permutationOptions.forEach((currentOption) => {
    smallerPermutations.forEach((smallerPermutation) => {
      permutations.push([currentOption].concat(smallerPermutation));
    });
  });

  return permutations;
}

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const info = arg.slice(1, M + 1);
    const p = arg.slice(-1)[0].split(" ").map(n=>parseInt(n));
    
    const combos = permutateWithRepetitions([0, 1], N);
    let answer = 0;

    for(let i in combos) {
        let lightOn = 0;

        for(let j=0; j<M; j++) {
            let temp = info[j].split(" ").map(n=>parseInt(n));
            let k = temp[0];
            let s = temp.slice(1, k + 1);
            
            let cnt = 0;
            
            for(let k=0; k<s.length; k++) {
                if(combos[i][s[k] - 1] === 1) cnt++;
            }

            if(cnt % 2 === p[j]) {
                lightOn++;
            }
        }
        
        if(lightOn === M) {
            answer++;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```