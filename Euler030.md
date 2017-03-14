#各位数字的五次幂
>令人惊讶的是，只有三个数可以写成它们各位数字的四次幂之和：
1634 = 14 + 64 + 34 + 44
8208 = 84 + 24 + 04 + 84
9474 = 94 + 44 + 74 + 44
由于1 = 14不是一个和，所以这里并没有把它包括进去。
这些数的和是1634 + 8208 + 9474 = 19316。
找出所有可以写成它们各位数字的五次幂之和的数，并求这些数的和。

```javascript
    var result1000000;
    result1000000 = 7 * Math.pow(9, 5);//7位数最大的五次幂之和为413343是六位数，范围为7位数以下
    var result100000;//六位数
    var result10000;//五位数
    var result1000;//四位数
    var result100;//三位数
    var result10;//二位数
    var sum = 0;
    for (var a = 0; a < 10; a++) {
        for (var b = 0; b < 10; b++) {
            result10 = Math.pow(a, 5) + Math.pow(b, 5);
            if ((result10 == a * 10 + b) && result10 >= 10 && result10 <= 99) {
                sum += result10;
                console.log("各位数字的五次幂之和的数" + result10);
            }
            for (var c = 0; c < 10; c++) {
                result100 = Math.pow(a, 5) + Math.pow(b, 5) + Math.pow(c, 5);
                if ((result100 == a * 100 + b * 10 + c) && result100 >= 100 && result100 <= 999) {
                    sum += result100;
                    console.log("各位数字的五次幂之和的数" + result100);
                }
                for (var d = 0; d < 10; d++) {
                    result1000 = Math.pow(a, 5) + Math.pow(b, 5) + Math.pow(c, 5) + Math.pow(d, 5);
                    if ((result1000 == a * 1000 + b * 100 + c * 10 + d) && result1000 >= 1000 && result1000 <= 9999) {
                        sum += result1000;
                        console.log("各位数字的五次幂之和的数" + result1000);
                    }
                    for (var e = 0; e < 10; e++) {
                        result10000 = Math.pow(a, 5) + Math.pow(b, 5) + Math.pow(c, 5) + Math.pow(d, 5) + Math.pow(e, 5);
                        if ((result10000 == a * 10000 + b * 1000 + c * 100 + d * 10 + e) && result10000 >= 10000 && result10000 <= 99999) {
                            sum += result10000;
                            console.log("各位数字的五次幂之和的数" + result10000);
                        }
                        for (var f = 0; f < 10; f++) {
                            result100000 = Math.pow(a, 5) + Math.pow(b, 5) + Math.pow(c, 5) + Math.pow(d, 5) + Math.pow(e, 5) + Math.pow(f, 5);
                            if ((result100000 == a * 100000 + b * 10000 + c * 1000 + d * 100 + e * 10 + f) && result100000 >= 100000 && result100000 <= 999999) {
                                sum += result100000;
                                console.log("各位数字的五次幂之和的数" + result100000);
                            }
                        }
                    }
                }
            }
        }
    }
    console.log("这些数的和" + sum);
```