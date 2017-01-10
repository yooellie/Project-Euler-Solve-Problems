#题目10：计算两百万以下所有质数的和。
>**注意：** 毕达哥拉斯三元组{a, b, c}。一个毕达哥拉斯三元组是一个包含三个自然数的集合，a<b<c，满足条件：
a^2 + b^2 = c^2 例如：3^2 + 4^2 = 9 + 16 = 25 = 5^2.
```javascript
        var arr = [];
        var sum = 0;
        for (var j = 2; j <= 2000000; j++) {
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
            sum += zs;
            j = zs;
        }
        console.log("两百万以下所有质数的和：" + sum);
```