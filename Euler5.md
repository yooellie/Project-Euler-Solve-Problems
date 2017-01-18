#题目5：找出最小的能被1-20中每个数整除的数。
> **注意：** 2520是最小的能被1-10中每个数字整除的正整数。
```javascript
    function gcd(a, b) {
        var minNum = Math.min(a, b);
        var maxNum = Math.max(a, b);
        var i = Math.floor(maxNum / minNum);
        var comMultiple = 0;

        for (; i <= maxNum; i++) {
            comMultiple = minNum * i;
            if (comMultiple % maxNum === 0) {
                min = comMultiple;
                return comMultiple;
            }
        }
    }
    var WITHIN_NO = 20;
    var min = 1;
    for (var j = 1; j <= WITHIN_NO; j++) {
        if (j == WITHIN_NO) {
            console.log(gcd(min, j));
        } else {
            gcd(min, j);
        }
    }
```
---
参考文献：[https://my.oschina.net/tearlight/blog/145135].
    