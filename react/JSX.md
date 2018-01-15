#### JSX语法

1. 严格区分大小写
2. 标签必须闭合
```js
<input type="text"/>
```
3. 一个js节点必须包裹在一个闭合标签内
```js
let ele = <h1>1</h1><h2>2</h2>
```
上面写法会报错
```js
let ele = <div>
           <h1>1</h1>
           <h2>2</h2>
          </div>
```
4. JSX内部嵌入js语法 使用大括号 大括号内部必须是值 可以是表达式 如运算表达式
```js
let a =10
<div> {a} </div>
```
表达式 如运算表达式
```js
const test = false
let a = 10
let ele = <div>
  { test ? <span>{a}</span> : <h1>100</h1>}
</div>
```
