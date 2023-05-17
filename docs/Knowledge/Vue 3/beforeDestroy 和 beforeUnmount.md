
`beforeDestroy`和`beforeUnmount`是Vue.js生命周期函数。 
它们的作用: 是在组件被销毁前执行一些清理操作。  
在Vue.js中，组件销毁的原因可能是因为它所在的父组件被销毁，或者它自己被销毁。

在Vue.js中，每个组件都有一个生命周期，它由一系列的生命周期钩子函数组成。这些函数在组件不同的生命周期阶段被调用。在这里，我们将讨论Vue.js的生命周期中的两个函数：`beforeDestroy`和`beforeUnmount`。

`beforeDestroy`是Vue 2.x版本中的生命周期钩子函数，而`beforeUnmount`是Vue 3.x版本中的新生命周期钩子函数。它们的作用相同，都在组件销毁之前被调用。

在这两个钩子函数中，你可以在这个钩子中执行一些清理操作，例如取消事件订阅、清除计时器、清除DOM事件监听器、取消网络请求等来释放资源。这些操作可以帮助你避免内存泄漏和不必要的资源占用。

这两个函数的具体实现会根据我们的需求而有所不同。下面是一些具体的例子：

- Vue 2.x版本中使用`beforeDestroy`
```js
export default {
  data () {
    return {
      timer: null
    }
  },
  created () {
    this.timer = setInterval(() => {
      console.log('timer running...')
    }, 1000)
  },
  beforeDestroy () {
    clearInterval(this.timer)
    // 执行一些清理操作 
    // 取消事件订阅、清除定时器等
  } 
}

```

- Vue 3.x版本中使用`beforeUnmount`
```ts
// 注册一个回调函数，在组件实例被卸载之后调用。
 function onUnmounted(callback: () => void): void
```

```vue
<script setup>
import { onMounted, onUnmounted } from 'vue'

let intervalId
onMounted(() => {
  intervalId = setInterval(() => {
    // ...
  })
})

onUnmounted(() => clearInterval(intervalId))
</script>
```

-   **详细信息**  
    一个组件在以下情况下被视为已卸载：  
    
    -   其所有子组件都已经被卸载。   
    -   所有相关的响应式作用 (渲染作用以及 `setup()` 时创建的计算属性和侦听器) 都已经停止。  
    
    可以在这个钩子中手动清理一些副作用，例如计时器、DOM 事件监听器或者与服务器的连接。
    
    **这个钩子在服务器端渲染期间不会被调用。**  

