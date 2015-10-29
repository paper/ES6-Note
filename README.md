# ES6 Note

### Math.trunc
Math.trunc() 方法会将数字的小数部分去掉，只留整数部分。  
https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc
```
Math.trunc = Math.trunc || function(value) {
    return value < 0 ? Math.ceil(value) : Math.floor(value);
}
```
```
// 【注意】这个比 parseInt 靠谱
parseInt(-2.22233413431e-15, 10)  // -2   error
Math.trunc(-2.22233413431e-15)  // -0   right
```
