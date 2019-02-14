## 组件名为多个单词

#### 组件名应该始终是多个单词的，根组件 App 除外。

这样做可以避免跟现有的以及未来的 HTML 元素相冲突，因为所有的 HTML 元素名称都是单个单词的。

>反例
```js
Vue.component('todo', {
  // ...
})
```
```js
export default {
  name: 'Todo',
  // ...
}
```

>好的例子
```js
Vue.component('todo-item', {
  // ...
})
```
```js
export default {
  name: 'TodoItem',
  // ...
}
```
## Prop定义

#### Prop 定义应该尽量详细。
在你提交的代码中，prop 的定义应该尽量详细，至少需要指定其类型。

?> 细致的 prop 定义有两个好处：  
它们写明了组件的 API，所以很容易看懂组件的用法；
在开发环境下，如果向一个组件提供格式不正确的 prop，Vue 将会告警，以帮助你捕获潜在的错误来源。
>反例
```js
// 这样做只有开发原型系统时可以接受
props: ['status']
})
```

>好的例子
```js
props: {
  status: String
}
```
```js
// 更好的做法！
props: {
  status: {
    type: String,
    required: true,
    validator: function (value) {
      return [
        'syncing',
        'synced',
        'version-conflict',
        'error'
      ].indexOf(value) !== -1
    }
  }
}
```