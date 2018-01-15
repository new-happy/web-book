## 数组的方法

### filter 过滤
```js
let objArr = [
  {name:'zhang',age:10},
  {name:'liu',age:13},
  {name:'wang',age:15}
]
let newArr = objArr.filter(item => item.age < 15)
console.log(newArr);
// findIndex 找到匹配条件的人的下标
// find找到匹配条件的人
let arr  = [1,2,3,4,5]
let num = arr.findIndex(item => item === 3)
console.log(arr[num])
let newArr = arr.map( item => item * item)
console.log(newArr)
```
### find

ES6 对数组的扩展中，有 find() 这个方法。用于找出**第一个**符合条件的数组成员。

find() 中传入的参数是什么呢？是一个函数，当一个函数被作为其他函数的参数的时候，这个函数就叫做一个**回调函数** （ callback function )。


```js
let data = [1, 5, 10, 15].find(value => value > 9) // 10

console.log(data)
```

上面，回调函数发挥的作用是判断条件。

### map 映射
map 的英文本意是：映射。map 把原始数组“变形了”：

- 输出依然是数组
- 输出的数组长度不变

#### 打怪

题：给定一个数组

```
let a = [1, 2, 3]
```

要得到一个新的数组 b ，值为

```
[2, 4, 6]
```

#### 答案

```
let a = [1, 2, 3]

let b = a.map(t => t*2)
console.log(b)
```

#### 理解上面的语法

上面的写法体现了函数式编程的思想。而函数式编程和面向对象编程一样，都是一种优秀的编程范式。

跟 map 类似的例子还有 filter/reduce 等。

### reverse 逆序

可以通过 array.reverse() 接口，将数组逆序输出。


#### 打怪

有数组 a

```
const a = [1, 2, 3, 4]
```

如何得到数组 b

```
[4, 3, 2, 1]
```

#### 答案

```js
const a = [1, 2, 3, 4]
const b = a.reverse()
```
