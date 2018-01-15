#### 导出
1. 命名导出
```js
let a = 10
let b = 20
let c = 30
export {a,b}
export {c}
```
命名导出必须加大括号

2. 默认导出
```js
export default a
```
默认导出只能导出一个  不用大括号

#### 导入
```js
import {a} from './App'
console.log(a);
import * as name from './App.js'
console.log(name)
import gg from './App.js'
console.log(gg);
import './App.js'
```
###### 注意
1. 命名导出时 导入必须与导出名一致且导入名必须加大括号
2. 默认导出时则可以不同名
3. 当想要把导出的内容全部导入的话 使用 (* as 变量) 导入

##### 第三方模块导入方法
```js
let _ = require('lodash')
console.log(_);
import map from 'lodash/map.js'
let arr = [5,8,4,9,9,5,8]
let num = findIndex.findIndex(arr,time => time === 8,2)
console.log(num);
```
