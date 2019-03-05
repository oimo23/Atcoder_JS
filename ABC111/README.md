### ABC114
[問題ページ](https://atcoder.jp/contests/abc111/tasks)

### A-AtCoder Beginner Contest 999
```JavaScript
'use strict'

function convertOneNine(target) {
    if(target == 1) return 9;
    if(target == 9) return 1;
}

function main(arg) {
    let answer = String(arg).split("").map(n=>convertOneNine(parseInt(n)));
    console.log(answer.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AtCoder Beginner Contest 111
```JavaScript
'use strict'

function main(arg) {
    let N = String(arg).split("").map(n=>parseInt(n));
    let answer;


    if( N[1] <= N[0] && N[2] <= N[0] ) {
        answer = String(N[0]) + String(N[0]) + String(N[0]);
        console.log(answer);
    } else {
        answer =  String(N[0]+1) + String(N[0]+1) + String(N[0]+1);
        console.log(answer);
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```