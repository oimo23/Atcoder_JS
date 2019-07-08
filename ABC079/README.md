### ABC079
[問題ページ](https://atcoder.jp/contests/abc079/tasks)

### A-Good Integer
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split("");

    if(N[0] == N[1] && N[1] == N[2] || N[1] == N[2] && N[2] == N[3]) {
        console.log("Yes");
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Lucas Number
```JavaScript
"use strict";
    
const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
	
    // 一部 JavaScript の扱える整数最大値を超えるので応急処置
    if (N === 77) {console.log("12360848946698171"); return;}
    if (N === 78) {console.log("20000273725560978"); return;}
    if (N === 79) {console.log("32361122672259149"); return;}
    if (N === 80) {console.log("52361396397820127"); return;}
    if (N === 81) {console.log("84722519070079276"); return;}
    if (N === 82) {console.log("137083915467899403"); return;}
    if (N === 83) {console.log("221806434537978679"); return;}
    if (N === 84) {console.log("358890350005878082"); return;}
    if (N === 85) {console.log("580696784543856761"); return;}
    if (N === 86) {console.log("939587134549734843"); return;}

    console.log(lucasMaster(N));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

function lucasMaster(n) {
  let answer = [2, 1];
  for ( let i = 2; i <= n; i++) {
    answer.push(answer[i-2] + answer[i-1]);
  }
  return answer.pop();
}

```