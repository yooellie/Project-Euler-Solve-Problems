### 题目4：找出由两个三位数乘积构成的回文。
> **注意：** 一个回文数指的是从左向右和从右向左读都一样的数字。最大的由两个两位数乘积构成的回文数是9009 = 91 * 99。

```javascript
    var arr = [];
    var max = 0;
    var maxi = 0;
    var maxj = 0;
    var maxVal = 0;
    for (var i = 899; i <= 999; i++) {
        for (var j = 899; j < 999; j++) {
            maxVal = i * j;
            //将字符串分割为数组
            arr = String(i * j).split("");
            //从左向右和从右向左读都一样的数字
            if ((arr[0] == arr[arr.length-1]) && (arr[1] == arr[arr.length-2]) && (arr[2] == arr[arr.length-3])) {
                if (parseInt(arr.join("")) > max) {
                    //找到最大的回文数字
                    max = parseInt(arr.join(""));
                    maxi = i;
                    maxj = j;
                }
            }
        }
    }
    alert("最大的三位数回文由" + maxi + "*" + maxj + "为" + max);
```