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

### C-直訴
```JavaScript
"use  strict";

const main = arg => {
  arg = arg.trim().split("\n");
  const dots = arg[0].split(" ").map(n=>parseInt(n));

  x = [dots[0], dots[1]];
  y = [dots[2], dots[3]];
  z = [dots[4], dots[5]];

  y = [y[0] - x[0], y[1] - x[1]];
  z = [z[0] - x[0], z[1] - x[1]];

  answer = ( (y[0] * z[1] - y[1]*z[0])/2)

  if(answer < 0){ answer = answer * -1; }
  answer = parseInt(answer * 10, 10)/10;

  console.log(answer);
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```