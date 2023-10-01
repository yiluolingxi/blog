`Vue.observable`是Vue 2.6.0版本引入的一个新特性，它可以使一个对象变得可响应。这意味着当这个对象的属性被改变时，Vue会自动检测到这些改变，并更新依赖这些属性的任何地方。

这个特性在某些情况下非常有用，例如，当你想在多个组件之间共享一些状态，但又不想使用Vuex这样的状态管理库时，你可以使用`Vue.observable`来创建一个可响应的状态对象。

以下是一个使用`Vue.observable`的例子：
```js
const state = Vue.observable({ count: 0 })

const Counter = {
  render(h) {
    return h('button', {
      on: { click: () => { state.count++ } },
    }, `count is: ${state.count}`)
  }
}
```
在这个例子中，我们首先使用`Vue.observable`创建了一个可响应的状态对象`state`。然后在`Counter`组件中，我们使用这个状态对象。当用户点击按钮时，`state.count`的值会增加，然后Vue会自动检测到这个改变，并更新按钮的内容。

需要注意的是，在Vue 3中，`Vue.observable`已经被`reactive`方法替代。