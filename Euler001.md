### 题目1：找出1000以下自然数中3和5的倍数之和。

```javascript
    var sum = 0;
    const WITHIN_NO = 1000;
    for (var i = 0; i < WITHIN_NO; i++) {
        if (i % 3 == 0 || (i % 5 == 0)) {
            sum += i;
        }
    }
```