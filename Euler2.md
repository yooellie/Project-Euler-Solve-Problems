#题目2：在斐波那契数列中，找出4百万以下的项中值为偶数的项之和。
>**注意：** 斐波那契数列中的每一项被定义为前两项之和。从1和2开始，斐波那契数列的前十项为：1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ...。
``` javascript
    function f(n) {
        if (n == 1) {
            return 1
        }
        if (n == 2) {
            return 2
        }
        return f(n - 1) + f(n - 2)
    }
    var sum = 0;
    for (var i = 1; f(i) <= 4000000; i++) {
        if (f(i) % 2 == 0) {
            sum += f(i);
        }
    }
    console.log(sum);
```