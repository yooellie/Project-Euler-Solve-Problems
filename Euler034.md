### 题目34：各位数字的阶乘
>145是个有趣的数，因为1! + 4! + 5! = 1 + 24 + 120 = 145。
找出所有各位数字的阶乘和等于其本身的数，并求它们的和。
注意：因为1! = 1和2! = 2不是和的形式，所以它们并不在讨论范围内。

```javascript
    var cj = 1;
    var arr = [];
    arr.push(1);//0的阶乘为1
    var result = 0;
    for (var i = 1; i < 10; i++) {
        cj *= i;
        arr.push(cj)
    }
    //    arr[9]*8<10000000, arr[9]*7>1000000所以这个数最大为七位数
    for (var a = 1; a < 10; a++) {
        for (var b = 0; b < 10; b++) {
            if ((String(a) + String(b)) == (arr[a] + arr[b])) {
                console.log(arr[a] + arr[b]);
                result += arr[a] + arr[b];
            }
            for (var c = 0; c < 10; c++) {
                if ((String(a) + String(b) + String(c)) == (arr[a] + arr[b] + arr[c])) {
                    console.log(arr[a] + arr[b] + arr[c]);
                    result += arr[a] + arr[b] + arr[c];
                }
                for (var d = 0; d < 10; d++) {
                    if ((String(a) + String(b) + String(c) + String(d)) == (arr[a] + arr[b] + arr[c] + arr[d])) {
                        console.log(arr[a] + arr[b] + arr[c] + arr[d]);
                        result += arr[a] + arr[b] + arr[c] + arr[d];

                    }
                    for (var e = 0; e < 10; e++) {
                        if ((String(a) + String(b) + String(c) + String(d) + String(e)) == (arr[a] + arr[b] + arr[c] + arr[d] + arr[e])) {
                            console.log(arr[a] + arr[b] + arr[c] + arr[d] + arr[e]);
                            result += arr[a] + arr[b] + arr[c] + arr[d] + arr[e];
                        }
                    }
                    for (var f = 0; f < 10; f++) {
                        if ((String(a) + String(b) + String(c) + String(d) + String(e) + String(f)) == (arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f])) {
                            console.log(arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f]);
                            result += arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f];
                        }
                    }
                    for (var g = 0; g < 10; g++) {
                        if ((String(a) + String(b) + String(c) + String(d) + String(e) + String(f) + String(g)) == (arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f] + arr[g])) {
                            console.log(arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f] + arr[g]);
                            result += arr[a] + arr[b] + arr[c] + arr[d] + arr[e] + arr[f] + arr[g];
                        }
                    }
                }
            }
        }
    }
    console.log("和为" + result);
```