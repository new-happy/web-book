#### 对象展开运算符
```js
var arr = [1,2,3]
var arr1 = [4,5,6]
var newArr = [...arr,...arr1]
console.log(newArr)

var obj = {
  name:'zzt',
  age:10
}
var obj1 = {
  say:function () {
    console.log(this.name)
  }
}
var newObj = {...obj,...obj1}
console.log(newObj);
```
