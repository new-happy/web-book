#### let es6声明变量的方式

1. 拥有块级作用域,只要在大括号内声明就会形成作用域
```js
 for (let i = 0; i < 3; i++) {   
   console.log('out',i)
  for (let i = 0; i < 2; i++) {
    console.log('in',i);
  }
}
```

2. 同一作用域下不允许重复声明相同变量
```js
let a = 10
let a = 20
```
es6上面这种声明会报错

3. 变量声明不提升
```
 console.log(a)
 let a = 10
```
4. const用来声明常量,不允许被修改
```js
const [a, b, c, d, e] = 'hello';
console.log(a + b + c + e);
```
