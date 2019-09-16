1. 基本类型包含7个
原始类型：number/string/boolean/symbol(Symbol 是 ES6 引入了一种新的原始数据类型，表示独一无二的值)
null/undefined
Object
其中object包含Array/Function/Regexp/Date

2. typeof
typeof 只返回 原始类型/函数/undefined/object
typeof []: object
typeof null: object
typeof Symbol(1): symbol

注意：
1）空数组[]的返回值是object，这表示，JavaScript内部，数组本质上是一种特殊的对象。

2）null的返回值是object，这是由于历史原因造成的，1995年JavaScript语言的第一版，所有值都设计成32位，其中最低的3位用来表述数据类型，
object对应的值是000。当时，只设计了五种数据类型（对象、整数、浮点数、字符串和布尔值），完全没考虑null，只把它当作object的一种特殊值，32位全部为0。
这是typeof null返回object的根本原因。
为了兼容以前的代码，后来就没法修改了。这并不是说null就属于对象，本质上null是一个类似于undefined的特殊值。

3.instanceof
instanceof 是判断变量是否为某个对象的实例，返回值为true或false
typeof 对数组 [] 和对象 {} 的返回值都是Object，无法区分数组和对象，但是instanceof可以区分。
注意： 数组Array是对象Object的一个子类，所以 a instanceof Object的返回值是 true。
var o = {};
var a = [];

o instanceof Array // false
a instanceof Array // true
a instanceof Object // true
