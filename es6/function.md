## 箭头函数
```js
function add(a,b) {
   console.log(a+b);
}
 add(a,b);
//现在
 let add = (a,b) => console.log(a+b);
```
注:参数大于一个的时候 必须使用小括号,当只有一个参数的时候可以省略小括号
```js
 let add = () => {
   var a = 10
   var b = 20
   var c = a + b
   return c
 }
 console.log(add())
```
### 箭头函数注意
1. 函数体内的this对象,就是定义时所在的对象,而不是使用时的对象
2. 不可以当做构造函数
3. 不可以使用arguments对象,可以使用rest参数代替

### es6 函数参数
参数的默认值 函数声明的时候在小括号内部直接给参数赋值相当于给了参数默认值

```js
function fun(x=0,y=0) {
  if(!x){
    x = 0
  }
  if(!y){
    y = 0
  }
  var a = x || 0
  var b = y || 0
  return x*y
}
var z = fun()
console.log(z)
```
### es6 函数参数的集合
```js
let sun = (a,...rest) => console.log(rest)
sun(1,2,3,4,5,6)
console.log(rest);
```
输出 [2,3,4,5,6]
rest 是剩余参数

### 为何要把函数弄得这么简短

因为 JS 特别强调**函数式编程**，也就是经常弄一些无名函数，作为另外一个高阶函数的参数，传来传去，那么这样定义函数时语句的简短就显得非常有必要了。

### 另外一个好处：this 穿透

老的函数写法，需要经常 bind(this) ，因为 this 是不穿透的，箭头函数默认可以让父作用域的 this 直接*穿透*进来，所以一般不需要 bind(this) 。

### 参考

- http://es6.ruanyifeng.com/#docs/function#箭头函数
- http://haoduoshipin.com/v/211.html