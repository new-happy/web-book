同伙改变字符串模板 改变 背景色
```js
import React,{ Component } from 'react'
import './box.css'

class Box extends Component {
  state = {
    active : true
  }
  handelClick = () => {
    this.setState({
      active : !this.state.active
    })
  }
  render () {
   return (
     <div className="box">
       <div className={`box-up ${this.state.active && 'active'}`}></div>
       <button onClick={ this.handelClick }>切换</button>
     </div>
   )
  }
}

export default Box
```
