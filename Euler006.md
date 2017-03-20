### 题目6：平方和与和平方的差是多少？

```javascript
    var sumSquare = 0;
    var squareSum = 0;
    for (var i = 1; i <= 100; i++) {
        squareSum += Math.pow(i, 2);
        sumSquare += i;
    }
    var val = Math.pow(sumSquare, 2) - squareSum;
    alert("前一百个自然数的平方和与和平方的差：" + val);
```