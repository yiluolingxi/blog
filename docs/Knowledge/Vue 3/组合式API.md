### setup()

关于什么的
有哪些关键词
哪些重要信息


组合式API是Vue3中引入的一种新的编程模式。它提供了一种更灵活的方式来组织和复用组件的逻辑。

在Vue2中，我们通常使用选项式API来编写组件，即在组件对象中定义一系列选项（如data、methods、computed、watch等）。这种方式在处理简单的逻辑时非常直观和方便，但在处理复杂的逻辑时，相关的代码可能会分散在不同的选项中，使得代码难以维护。

组合式API通过引入`setup`函数，允许我们在一个单独的函数中组织和复用逻辑。在`setup`函数中，我们可以使用一系列新的Vue函数（如`ref`、`reactive`、`computed`、`watch`等）来创建和管理响应式的数据和副作用。

例如，以下是一个使用组合式API的例子：  
```js
import { ref, computed } from 'vue'

export default {
  setup() {
    const count = ref(0)
    const double = computed(() => count.value * 2)

    function increment() {
      count.value++
    }

    return {
      count,
      double,
      increment
    }
  }
}
```
在这个例子中，我们在`setup`函数中创建了一个响应式的`count`，一个计算属性`double`，以及一个方法`increment`。然后我们将它们返回，使得它们可以在模板和其他地方使用。