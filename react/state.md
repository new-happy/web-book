#### react的stat
组件默认有一个 state 属性,这个属性是一个对象
1. constructor 方法下 设置state
```js
constructor () {
  super()
  this.state = {
    num : 1   //设置状态
  }
}
```
2. 胖箭头函数的方法设置state
```js
state = {
  num : 2
}
```
##### 更改state
```js
  handleClick = () => {
    let { num } = this.state
    this.setState({
      num : num + 1
    })
  }
  ```

state 状态, 组件的 state 变, 组件就会重新渲染,页面也就改变了
