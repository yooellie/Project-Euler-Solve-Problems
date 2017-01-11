#题目7：找出第10001个质数。
```javascript
    var arr = [];
    const PRIME_SERIAL_NO = 10000;
    for (var j = 2; arr.length <= PRIME_SERIAL_NO; j++) {
        IfPrimeNo(j);
    }

    //如果用2到根号zs之间的所有整数去除，均无法整除，则zs为质数。
    function IfPrimeNo(zs) {
        for (var i = 2; i <= Math.sqrt(zs); i++) {
            if (zs % i == 0) {
                return false;
            }
        }
        arr.push(zs);
    }
    alert("第10001个质数：" + arr[PRIME_SERIAL_NO]);
```