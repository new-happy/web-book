#### calss  类

es6 类的写法
```js
 class Person {
   constructor(name) {
     this.firstName = name
   }
   say(){
     console.log('hello')
   }
 }
 ```
class内部只能写方法,并且方法之间不能加逗号
onstructor函数 当执行new + class名 就会默认执行
```js
let people = new Person('sj')
console.log(people);
people.say()
class Son extends Person{
constructor(name,firstName) {
super(firstName) //处理this指向 如果继承的话必须向子类constructor内部必须添加super() 向super内部传参 相当于向继承的父级传参
  }
   jump(){
     console.log('jump')
 }
 }
 let son = new Son('djf','sj')
 son.say()

Object.assign() //合并两个对象
let obj = {
  name:'lll',
  age:10
}
var obj1 = Object.assign({},obj,{tall:'100'})
console.log(obj1,obj);
```
