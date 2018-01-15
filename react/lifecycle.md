生命周期函数也是 React 的核心概念。

一个 React 组件是有一定的生命周期的（从无到有，从有到新，从新到无）。

生命周期是以下面几个大事件为标志的：

- 首先是显示，也就是挂载（ mount ）到页面上
- 当 props 或者 state 被更新的时候，render 函数会被再次执行
- 组件从页面上消失，也就是卸载（ unmount ）

围绕上面这几个事件的前后，有几个 React 预先定义好的，可以自动触发的函数，这些函数叫做**生命周期函数**。

### 详细说明

- componentWillMount ，组件即将挂载，执行时间点是：组件被挂载到页面上之前的一瞬间
- componentDidMount ，组件已挂载，执行时间点，是组件刚刚被挂载到页面后（render 被执行后）的一瞬间
- componentWillUnmount ，组件即将被卸载，执行时间点是，组件从页面上消失之前
- 其他的还是，比如 componentWillReceiveProps 等等

### 作用

- 自动触发 http 请求
- 自动清理程序垃圾

作用很多，后面会有很多实际例子可以看到。


### 例子

```js
import React, { Component } from 'react'
import './app.css'

class App extends Component {

  state = {
    count: 0
  }
  componentWillMount = () => {
    console.log('componentWillMount....')
  }

  componentDidMount = () => {
    console.log('componentDidMount....')
  }

  handleClick = () => {
    this.setState({
      count: this.state.count + 1
    })
  }

  componentWillUpdate = ()  => {
    console.log('componentWillUpdate...')
  }

  componentDidUpdate = () => {
    console.log('componentDidUpdate...')
  }

  render () {
    console.log('render.......')
    return (
      <div className='app'>
        <div onClick={this.handleClick}
          className='count'>
          {this.state.count}
        </div>
      </div>
    )
  }
}

export default App
```

### 视频

- http://digicity-1253322599.costj.myqcloud.com/life-cycle.mp4
