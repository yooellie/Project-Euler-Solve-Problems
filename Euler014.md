### 题目14：最长考拉兹序列
>**注意：** 在正整数集上定义如下的迭代序列：
n → n/2 （若n为偶数）
n → 3n + 1 （若n为奇数）
从13开始应用上述规则，我们可以生成如下的序列：
13 → 40 → 20 → 10 → 5 → 16 → 8 → 4 → 2 → 1
可以看出这个序列（从13开始到1结束）共有10项。尽管还没有被证明，但我们普遍认为，从任何数开始最终都能迭代至1（“考拉兹猜想”）。
从小于一百万的哪个数开始，能够生成最长的序列呢？
注： 序列开始生成后允许其中的项超过一百万。

```javascript
    var arr = [];
    var a = 1;
    var maxLength = 0;
    var max = 0;
    for (var i = 1; i < 1000000; i++) {
        arr[i] = [i];
        for (a = i; a > 1;) {
            if (a % 2 == 0) {
                a = a / 2;
            } else {
                a = 3 * a + 1;
            }
            if (a > i) {
                arr[i].push(a);
            }
            else {
                arr[i].length += arr[a].length;
                break;
            }
        }
        if (arr[i].length > maxLength) {
            maxLength = arr[i].length;
            max = arr[i][0];
        }
    }
    console.log(max);
```

