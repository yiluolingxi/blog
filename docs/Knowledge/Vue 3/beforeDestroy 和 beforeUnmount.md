
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


---

### 追根究底

- 
```ts
function onUnmounted(callback: () => void): void
```
这段代码是一个函数定义，用于在组件卸载（Unmounted）时执行一个回调函数。

这行代码定义了一个函数 `onUnmounted`，它接受一个回调函数 `callback` 作为参数，并且不返回任何值（`void`）。

`callback: () => void`

这里使用了 TypeScript 的类型注解，指定了 `callback` 参数的类型。`() => void` 是一个函数类型的注解，表示这个函数没有任何参数（`()`）并且不返回任何值（`void`）。

`: void`

这个部分是函数的返回类型注解，指定了函数没有返回值。

因此，这个函数的作用是在组件卸载时执行传递进来的回调函数。通常在编写组件时，我们需要在组件被卸载之前做一些清理工作，比如取消订阅、清除定时器、释放资源等。这个函数可以方便地将这些清理操作与组件的生命周期绑定起来，确保在组件卸载时执行相应的清理逻辑。



- 
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

在这段代码中，我们首先导入了 `onMounted` 和 `onUnmounted` 函数，这是Vue 3提供的生命周期钩子函数。

接下来，我们声明了一个名为 `intervalId` 的变量，用于保存 `setInterval` 函数返回的计时器ID。

然后，我们在 `onMounted` 钩子函数中调用了 `setInterval` 函数。`setInterval` 函数用于按照指定的时间间隔循环执行给定的代码块。在这个例子中，我们省略了代码块的具体内容（`// ...`），你可以在这里编写你需要循环执行的逻辑。

通过将计时器ID赋值给 `intervalId` 变量，我们在组件的生命周期中保留了对计时器的引用。

最后，在 `onUnmounted` 钩子函数中，我们调用了 `clearInterval` 函数，并传入之前保存的 `intervalId` 变量，以取消定时器的执行。这确保在组件销毁之前，计时器被正确清除，以防止内存泄漏。

总结来说，这段代码的功能是在组件挂载时创建一个定时器，然后在组件卸载时清除该定时器，以确保正确管理和释放资源。
