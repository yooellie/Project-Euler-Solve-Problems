### 题目21：亲和数
>记d(n)为n的所有真因数（小于n且整除n的正整数）之和。如果d(a) = b且d(b) = a，且a ≠ b，那么a和b构成一个亲和数对，a和b被称为亲和数。
例如，220的真因数包括1、2、4、5、10、11、20、22、44、55和100，因此d(220) = 284；而284的真因数包括1、2、4、71和142，因此d(284) = 220。
求所有小于10000的亲和数的和。

```javascript
    var arr = [];
    var result = 0;
    for (var i = 1; i < 10000; i++) {
        var sum = 1;
        for (var j = 2; j <= i / 2; j++) {
            if (i % j == 0) {
                sum += j;
            }
        }
        arr[i] = sum;
        for (var k = 0; k < arr.length; k++) {
            if (arr[k] == i && arr[i] == k && k != i) {
                result += k + i;
            }
        }
    }
    alert("所有小于10000的亲和数的和" + result);
```