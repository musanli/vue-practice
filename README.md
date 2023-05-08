[参考文档](https://cn.vuejs.org/guide/introduction.html])


## 指令
指令带有前缀 v-，以表示它们是 Vue 提供的特殊 attribute。
`<span v-bind:title="message"></span>`
### 事件监听器 v-on
为了让用户和你的应用进行交互，我们可以用 v-on 指令添加一个事件监听器，通过它调用在 Vue 实例中定义的方法：

### vue 自身提供指令
v-model 双向绑定


Vue 生命周期钩子的 this 上下文指向调用它的 Vue 实例
Vue 实例还暴露了一些有用的实例 property 与方法。它们都有前缀 $，以便与用户定义的 property 区分开来。

```shell
# 查看当前项目vue 版本
npm list vue 
npm view create-vue
npm view create-vue versions
npm init vue@2.1.1
```
#### 什么是 node 什么是 npm
Node.js是一个基于Chrome V8引擎的JavaScript运行环境，可以在服务器端运行JavaScript代码。它可以让开发人员使用JavaScript语言开发服务器端应用程序，包括Web应用程序、命令行工具等。
npm（Node Package Manager）是Node.js的包管理器，它可以帮助开发人员在自己的项目中安装、管理和分享代码包。npm是世界上最大的开源软件注册表，拥有超过100万个包，可以帮助开发人员轻松地使用这些包来构建自己的应用程序。



每个 Vue 应用都是通过用 Vue 函数创建一个新的 Vue 实例开始的：
```vue
var vm = new Vue({
  // optional
})
```


**只有当实例被创建时就已经存在于 data 中的 property 才是响应式的**
![https://v2.cn.vuejs.org/images/lifecycle.png](https://v2.cn.vuejs.org/images/lifecycle.png)
VUE 生命周期方法
beforCreate-->created-->beforeMount-->mounted-->beforeDestroy-->destoryed

不要在选项 property 或回调上使用箭头函数，比如 created: () => console.log(this.a) 或 vm.$watch('a', newValue => this.myMethod())。因为箭头函数并没有 this，this 会作为变量一直向上级词法作用域查找，直至找到为止，经常导致 Uncaught TypeError: Cannot read property of undefined 或 Uncaught TypeError: this.myMethod is not a function 之类的错误。

