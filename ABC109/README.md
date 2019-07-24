### ABC109
[問題ページ](https://atcoder.jp/contests/abc109/tasks)

### A-ABC333
```JavaScript
"use strict";

const main = input => {
    input = parseInt(input);

    if(input == 7 || input == 5 || input == 3) {
      console.log("YES");
    } else {
      console.log("NO");
    }
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));
```

### B-Shiritori
```JavaScript
"use strict";

const main = arg => {
    const N     = parseInt(arg.split("\n")[0]);
    const words = arg.split("\n").slice(1);
    const memo  = new Set();

    let lastLetter = words[0].slice(0, 1);

    for(let i=0; i<N; i++) {
        if(lastLetter !== words[i].slice(0, 1) || memo.has(words[i])) {
            console.log('No');
            return;
        }

        lastLetter = words[i].slice(-1);
        memo.add(words[i]);
    }
    
    console.log('Yes');
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Skip
```JavaScript
"use strict";

const getGcd = (input) => {
  let len, a, b;
	len = input.length;
	a = input[0];
	for (let i=1; i<len; i++) {
		b = input[i];
		a = gcdTwoNumbers(a, b);
	}
	return a;
}

const gcdTwoNumbers = (x, y) => {
  x = Math.abs(x);
  y = Math.abs(y);
  while(y) {
    let t = y;
    y = x % y;
    x = t;
  }
  return x;
}

const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const X = parseInt(arg[0].split(" ")[1]);
    const numbers = arg[1].split(" ").map(n=>parseInt(n));
    
    const evenOdd = numbers.filter(n=>n % 2 === 0).length;
    
    if(N === 1) {
        console.log(Math.abs(numbers[0] - X));
        return;
    }

    let list = [];
    
    for(let i=0; i<N; i++) {
        let temp = Math.abs(numbers[i] - X);
        list.push(temp);
    }
    
    console.log(getGcd(list));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```