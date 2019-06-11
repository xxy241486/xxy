## 解构赋值

### 1.数组的解构赋值
```
let [a, b, c] = [1, 2, 3];
let [x, y = 'b'] = ['a']; // x='a', y='b'
```
### 2.对象的解构赋值
```
let { foo, bar } = { foo: 'aaa', bar: 'bbb' };
foo // "aaa"
bar // "bbb"

let { baz } = { foo: 'aaa', bar: 'bbb' };
baz // undefined
```
### 3.字符串的解构赋值
```
const [a, b, c, d, e] = 'hello';
a // "h"
b // "e"
c // "l"
d // "l"
e // "o"

let {length : len} = 'hello';
len // 5
```
