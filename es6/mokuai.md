#### node模块分三类
1. 核心模块(自带的)
2. 文件模块(自己写的)
3. 第三方模块(插件)

##### 文件模块引入
```js
function fun(x,y) {
  console.log(x+y);
 }
module.exports = fun
```
module.exports 导出模块
```js
var b = require('./index.js')
b(5,6)
```
require 导入模块 (路径)

#### 第三方模块导入
```js
 var $ = require('jquery')
 console.log($);
```
这里nodejs会去node_modules里面找到package.json文件,找到面字段里面的入口文件
