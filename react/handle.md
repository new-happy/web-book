#### react绑定事件
1. 给react 组件绑定事件 必须使用行内事件方式绑定  事件名称 驼峰命名
```js
handleClick1 = () => {
    console.log(this)
  }
  render() {
    let a = 10
    return (
      <div className="App">
        <span>{ this.state.num}</span>
          <button onClick={() => this.handleClick(a)}>加</button>

      </div>
    );
  }
```
2. 有个问题 就是就是当在行内绑定事件的时候 事件函数内部的 this就会指向window 所有在组件内部
声明事件函数的时候 通常使用箭头函数
3. 也可以使用constructor方法 改变this的指向
也可以使用constructor方法 改变this的指向
```js
constructor(){
    super()
    this.handleClick=this.handleClick.bind(this) //更改this指向
  }
```
react的事件函数的最后一个参数默认是事件对象
4. react事件  http://wiki.jikexueyuan.com/project/react/event-system.html
