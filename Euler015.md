#网格路径
>**注意：** 从一个2×2方阵的左上角出发，只允许向右或向下移动，则恰好有6条通往右下角的路径。对于20×20方阵来说，这样的路径有多少条？

```javascript
//    (2n)!/n!
var sum0 = 1;
var sum1 = 1;
for (var i = 40; i > 20; i--) {
sum0 *= i;
}
for (var j = 20; j > 1; j--) {
sum1 *= j;
}
console.log(parseInt(sum0 / sum1));
```