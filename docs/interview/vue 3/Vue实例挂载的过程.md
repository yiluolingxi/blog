在Vue 3中，如果你使用组合式API（Composition API），Vue实例的挂载过程主要包括以下几个步骤：  
1. 创建应用：首先，使用`createApp`函数创建一个新的Vue应用实例。  
```js
const app = Vue.createApp(App)
```
2. 使用组合式API：在你的组件中，你可以使用`setup`函数来使用组合式API。在`setup`函数中，你可以定义和返回响应式数据、计算属性、方法等。  
```js
export default {
  setup() {
    // 在这里使用组合式API...
  }
}
```
3. 挂载：然后，使用`mount`方法将Vue应用实例挂载到指定的DOM元素上。  
```js
app.mount('#app')
```
在挂载过程中，Vue会执行以下操作：

- 初始化应用实例，包括设置其生命周期、事件、props、methods、data、computed和watch等。
- 执行`setup`函数，并收集其返回的响应式数据、计算属性、方法等。
- 如果提供了模板，Vue会将模板编译成渲染函数。如果没有提供模板，但是提供了render函数，Vue会直接使用这个函数。
- 执行渲染函数，生成虚拟DOM，并更新真实DOM。

4. 更新：当数据变化时，Vue会重新执行渲染函数，生成新的虚拟DOM，并与旧的虚拟DOM进行对比，计算出最小的更新范围，然后更新真实DOM。

以上就是在Vue 3的组合式API中，Vue实例挂载的基本过程。