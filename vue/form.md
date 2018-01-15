## 提交评论

来完成表单提交评论的功能。

#### 事件处理

可以参考官方事件处理的文档：https://cn.vuejs.org/v2/guide/events.html
```js
CommentBox.vue

    methods: {
      submitComment () {
        console.log('submitComment')
      }
    }
```
到 script 下，跟 data 和 computed 平级，添加 methods 也就是“方法”这一项。值是一个对象，里面就可以定义函数了。submitComment 中，暂时只打印一个字符串。

    <button @click="submitComment">提交</button>
模板中，添加一个按钮 button ，添加事件可以用 v-on: ，或者用 at 符，后面跟上事件名，这里是 click 。等号后面的双引号中，添加方法名。

浏览器中，点按钮，发现 submitComment 确实可以执行。

#### 获取表单中填写的内容

主要参考表单文档 https://cn.vuejs.org/v2/guide/forms.html 采用 v-model 的形式来获取。

先来看看 v-model 怎么使用。
```js
<template>
  <div class="comment-box">
    <input v-model="message" placeholder="请填写评论" />
    <button @click="submitComment">提交</button>
  </div>
</template>

<script>
  export default {
    name: 'CommentBox',
    data: () => ({
      message: '',
    }),
    methods: {
      submitComment () {
        console.log('submitComment', this.message)
        this.message = ''
      }
    }
  }
</script>

<style scoped>
  .comment-box {
    background-color: #fff;
    width: 400px;
    min-height: 30vh;
    margin: 20px auto;
    box-shadow: 0 2px 2px rgba(0, 0, 0, 0.5);
  }
</style>
```
v- 的作用是提示编译环境这不是一个 html 的原生属性，而是一个 vue 指令。model 的意思是数据模型，在这里我们简单理解为数据就行。

使用 v-model 有三个注意点：

第一，要使用 v-model 指令，等号后面是一个字符串，里面写变量名，这里是 message
第二，变量要声明一下才能使用，也就是要到 data 里面，添加 message 冒号，值是空字符串
第三，真正在 script 标签中用的时候，变量名前面要添加 this
这样，我们就可以在 submitComment 方法中打印出用户的输入了。

浏览器中，输入内容，然后点提交按钮。终端中可以打印出输入内容。