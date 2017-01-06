#题目1：找出1000以下自然数中3和5的倍数之和。
```javascript
    var sum = 0;
    for (var i = 0; i < 1000; i++) {
        if (i % 3 == 0 || (i % 5 == 0)) {
            sum += i;
        }
    }
```