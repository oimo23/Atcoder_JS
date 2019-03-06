### ABC104
[問題ページ](https://atcoder.jp/contests/abc104/tasks)

### A-Rated for Me
```JavaScript
function main(arg) {
    arg = parseInt(arg);
    
    if( arg < 1200 ){
        console.log("ABC");
    } else if( arg < 2800 ) {
        console.log("ARC")
    } else {
        console.log("AGC")
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AcCepted
```JavaScript
'use strict';

function main(arg) {
    arg = arg.split("\n");
    arg = arg[0];
    
    const indexA = arg.indexOf("A");
    const indexC = arg.indexOf("C");
    
    if(arg.split("").filter(n=>isLowerCase(n)).length !== arg.length - 2 ) {
        console.log("WA");
        return;
    }
    
    if(indexA === 0 && indexC >= 2 && indexC <= arg.length - 2) {
        console.log("AC");
    } else {
        console.log("WA");
    }
}

function isLowerCase(str){
    return str.match(/^[a-z]+$/) ? true: false;
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```