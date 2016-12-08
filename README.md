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
```
<p v-if="seen">Now you see me</p>
这里， v-if 指令将根据表达式 seen 的值的真假来移除/插入 <p> 元素
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
