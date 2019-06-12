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

## Iterator

### 作用：

1.为各种数据结构，提供一个统一的、简便的访问接口；（Array/Object/Map/Set）

2.使得数据结构的成员能够按某种次序排列；

3.ES6 创造了一种新的遍历命令for...of循环，Iterator 接口主要供for...of消费。

```
function makeIterator(array) {
  var nextIndex = 0;
  return {
    next: function() {
      return nextIndex < array.length ?
        {value: array[nextIndex++]} :
        {done: true};
    }
  };
}
```
### for...of

Iterator 接口的目的，就是为所有数据结构，提供了一种统一的访问机制，即for...of循环（详见下文）。当使用for...of循环遍历某种数据结构时，该循环会自动去寻找 Iterator 接口。

原生具备 Iterator 接口的数据结构如下。

Array
Map
Set
String
TypedArray
函数的 arguments 对象
NodeList 对象

