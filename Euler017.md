#表达数字的英文字母计数
>如果把1到5写成英文单词，分别是：one, two, three, four, five，这些单词一共用了3 + 3 + 5 + 4 + 4 = 19个字母。
如果把1到1000都写成英文单词，一共要用多少个字母？
注意： 不要算上空格和连字符。例如，342（three hundred and forty-two）包含23个字母，而115（one hundred and fifteen）包含20个字母。
单词“and”的使用方式遵循英式英语的规则。

```javascript
    var str0109 = "one,two,three,four,five,six,seven,eight,nine";
    var str10 = "ten";
    var str1119 = "eleven,twelve,thirteen,fourteen,fifteen,sixteen,seventeen,eighteen,nineteen";
    var str2090 = "twenty,thirty,forty,fifty,sixty,seventy,eighty,ninety";
    var str100 = "hundred";
    var strhe = "and";
    var str1000 = "onethousand";
    var sum;
    function num(no) {
        var len = 0;
        no.split(",").forEach(function (e) {
            len += e.length;
        });
        return len;
    }
    var no0109 = num(str0109);//36 数字1-9
    var no10 = num(str10);//3 数字10
    var no1119 = num(str1119);//67 数字11-19
    var no2090 = num(str2090);//46 数字20，30，40，50
    var no100 = num(str100);//10 百
    var nohe = num(strhe);//3 和
    var no1000 = num(str1000);//11 //数字1000
    sum = (no0109 + no10 + no1119 + (no2090) * 10 + no0109 * 8) * 10 + (no100 * 9 + no0109) * 100 + nohe * 99 * 9 + no1000;
```