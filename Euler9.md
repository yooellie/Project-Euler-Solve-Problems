##题目9：已知存在并且只存在一个毕达哥拉斯三元组满足条件a + b + c = 1000。找出该三元组中abc的乘积
>**注意：** 毕达哥拉斯三元组{a, b, c}。一个毕达哥拉斯三元组是一个包含三个自然数的集合，a<b<c，满足条件：
a^2 + b^2 = c^2 例如：3^2 + 4^2 = 9 + 16 = 25 = 5^2.

```javascript
    var IfExist = false;
    for (var c = 1; c < 1000; c++) {
        for (var b = 1; b < c; b++) {
            for (var a = 1; a < b; a++) {
                if (Math.sqrt(a * a + b * b) === (1000 - a - b)) {
                    //只打印一次
                    if (!IfExist) {
                        var cVal = 1000 - a - b;
                        var abc = a * b * cVal;
                        console.log("a:" + a + " b:" + b + " c:" + cVal + " a*b*c:" + abc);
                    }
                    IfExist = true;
                    break;
                }
            }
        }
    }
```
