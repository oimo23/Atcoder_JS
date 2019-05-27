### ABC029
[問題ページ](https://atcoder.jp/contests/abc029/tasks)

### A-複数形
```JavaScript
"use strict";

const main = arg => {
    const S = arg.split("\n")[0];
    
    console.log(S + "s");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-カキ
```JavaScript
"use strict";
    
const main = arg => {
    const S    = arg.trim().split("\n");
    let answer = 0;
    
    for(let i in S) {
        if(S[i].indexOf("r") !== -1) {
            answer++;
        }    
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Brute-force Attack
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
    const N = parseInt(arg[0]);
    const list = ["a", "b", "c"];
    
    const answer = permutateWithRepetitions(list, N);
    
    console.log(answer.map(n=>n.join("")).join("\n"))
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```
