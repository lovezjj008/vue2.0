# vue2.0基础学习


### 1.模板语法
1.文本

```html
<span>Message: {{ msg }}</span>   文本插值
```
2.纯HTML
```html
<span>Message: {{{msg }}}</span>   HTML 输出
```
3.属性绑定   ==>  (href , checked, disabled, id ,title, name.......)
不能在 HTML 属性中使用，应使用 v-bind 指令:
```html
<div v-bind:id="true"></div>   缩写形式：<div :id="true"></div>
```
4.使用js语法绑定
```html
{{ number + 1 }}
{{ ok ? 'YES' : 'NO' }}
{{ message.split('').reverse().join('') }}
<div v-bind:id="'list-' + id"></div>
```
这些表达式会在所属 Vue 实例的数据作用域下作为 JavaScript 被解析。有个限制就是，每个绑定都只能包含单个表达式，所以下面的例子都不会生效。
```
<!-- 这是语句，不是表达式 -->
{{ var a = 1 }}
<!-- 流控制也不会生效，请使用三元表达式 -->
{{ if (ok) { return message } }}
``` 
5.指令
指令（Directives）是带有 v- 前缀的特殊属性。

```html
<p v-if="seen">Now you see me</p>
```
```
这里， v-if 指令将根据表达式 seen 的值的真假来移除/插入 <p> 元素
```
```
另一个例子是 v-on 指令，它用于监听 DOM 事件：click, keyup, hover ......
```
```html
<a v-on:click="doSomething">   
v-on缩写为 :click
```
### 2.条件渲染
1.v-if,  v-show  控制显影。
```html
<h1 v-if="ok">Yes</h1>
```
### 3.列表渲染
v-for
```html
<ul id="example-1">
  <li v-for="item in items">
    {{ item.message }}
  </li>
</ul>

</br>
```
```
var example1 = new Vue({
  el: '#example-1',
  data: {
    items: [
      {message: 'foo' },
      {message: 'Bar' }
    ]
  }
})
```
结果：
``` markdown
foo
Bar
```

### 3.表单控件绑定
你可以用 v-model 指令在表单控件元素上创建双向数据绑定
```html
<input v-model="message" placeholder="edit me">
<p>Message is: {{ message }}</p>

单个勾选框，逻辑值：

<input type="checkbox" id="checkbox" v-model="checked">
<label for="checkbox">{{ checked }}</label>
```










### 学习资料
- [vue官网](http://cn.vuejs.org)
- [ES6语法学习](http://es6.ruanyifeng.com/)
- [ESlint语法对照](http://www.tuicool.com/articles/rIFBfey)
- [UI组件:vue-strap](http://yuche.github.io/vue-strap/)
- [ajax调用组件:vue-resource](http://github.com)
- [路由组件:vue-router](http://github.com)
- [复杂状态管理:vuex](http://github.com)
- [docs for vue-loader](http://vuejs.github.io/vue-loader).
- [webpack vue guide](http://vuejs-templates.github.io/webpack/)
