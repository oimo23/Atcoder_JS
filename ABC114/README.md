### ABC114
[問題ページ](https://atcoder.jp/contests/abc114/tasks)

### A-753
```JavaScript
function Main(input) {
    parseInt(input);
    if( input == 7 || input == 5 || input == 3 ) {
      console.log("YES");
    } else {
      console.log("NO");
    }
}
Main(require("fs").readFileSync("/dev/stdin", "utf8"));

```

### B-754
```JavaScript
"use strict";

function Main(input) {
    parseInt(input);
    let num = input.split("");
    
    let diff = [];
    
    for ( var i=0; i<num.length; i++) {
        var temp = num.slice(i, i+3).join("");
        diff.push(Math.abs( 753 - temp ));
    }
    
    let answer = diff.reduce((n, m) => n <= m? n: m);
    console.log(answer);
    
}
Main(require("fs").readFileSync("/dev/stdin", "utf8"));

```