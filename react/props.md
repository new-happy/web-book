#### props方法

1. props传递与接收

```js
<div className="app">
   <Button name='用户名'/>
   <Button text='password'/>
</div>
//父组件通过组件传递数据
let { name,text } = this.props
     let val = 280
   return (
     <div className="button">
  <input type="text" placeholder={name} style={ {'width':val+'px','backgroundColor':'red'} }/>
  <button>{ text }</button>
```
```js
let { name,text} = this.props
    let styles = {
      username:{
        backgroundColor:'red'
      },
      password:{
        backgroundColor:'teal'
      }
    }
    let style = name ? styles.username : styles.password
   return (
     <div className="button">
        <input type={ text || 'text' } placeholder={ name || '密码'} style={ style }/>
     </div>
```
注意:
1. react 组件内部有一个默认参数叫 props 作用是接收父组件传过来的参数
如果是函数组件 函数第一个参数默认就是props
如果是es6 class组件的话组件内部用 this.props获取props
2. props对象是只读的 不能进行修改
当父组件传给子组件一个react节点的时候,子组件使用this.props.children接收
