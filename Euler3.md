#题目3：找出一个合数的最大质数因子
```javascript
    //n为合数
    var n = 600851475143;
    var max = 0;
    //因为n里面的质数范围为2到根号
    for (var j = 2; j <= Math.sqrt(n); j++) {
        //先算出因子
        if (n % j == 0) {
            //再算出因子中的质数
            IfPrimeNo(j);
        }
    }

    //如果用2到根号zs之间的所有整数去除，均无法整除，则zs为质数。
    function IfPrimeNo(zs) {
        for (var i = 2; i <= Math.sqrt(zs); i++) {
            if (zs % i == 0) {
                return false;
            }
        }
        if (zs > max) {
            max = zs;
        }
    }
    console.log(max);
			
```