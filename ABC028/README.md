### ABC028
[問題ページ](https://atcoder.jp/contests/abc028/tasks)

### A-テスト評価
```JavaScript
'use strict';

function main(arg) {
    console.log(arg.split(" ")[0] % arg.split(" ")[1] === 0 ? 0 : 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-文字数カウント
```JavaScript
'use strict';

function main(arg) {
    const N = parseInt(arg.split("\n")[0]);
    
    if(N < 4) {
        console.log("No");
        return;
    }
    
    if(N % 4 === 0 || N % 7 === 0 ) {
        console.log("Yes");
        return;
    }
    
    for(let i=0; i<N; i=i+4) {
        if((N - i) % 7 === 0) {
            console.log("Yes");
            return;
        }
    }
    
    for(let i=0; i<N; i=i+7) {
        if((N - i) % 4 === 0) {
            console.log("Yes");
            return;
        }
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-数を3つ選ぶマン
```JavaScript
"use strict";

const combineWithoutRepetitions = (comboOptions, comboLength) => {
  if (comboLength === 1) {
    return comboOptions.map(comboOption => [comboOption]);
  }

  const combos = [];
  
  comboOptions.forEach((currentOption, optionIndex) => {
    const smallerCombos = combineWithoutRepetitions(
      comboOptions.slice(optionIndex + 1),
      comboLength - 1
    );

    smallerCombos.forEach((smallerCombo) => {
      combos.push([currentOption].concat(smallerCombo));
    });
  });

  return combos;
}

const main = arg => {
    arg = arg.trim().split("\n");
    const N = arg[0].split(" ").map(n=>parseInt(n));
    
    const combos = combineWithoutRepetitions(N, 3);
    const list = [];
    
    for(let combo of combos) {
        list.push(combo.reduce((m,n)=>m+n));
    }
    
    const answer = new Set(list.sort((a,b)=>b-a));
    
    console.log([...answer][2]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
