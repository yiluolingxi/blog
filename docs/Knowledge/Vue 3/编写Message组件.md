首先定义了一个名为`msg`的prop，它是一个字符串。然后在`setup`函数中，我们使用`ref`函数创建了一个响应式引用`message`，并将它的初始值设置为`props.msg`。在模板中，我们使用`{{ message }}`来显示这个响应式引用的值。

这种方式的好处是，我们可以在`setup`函数中组织和复用逻辑，使得代码更加清晰和易于维护。  

---

在Vue3中，你可以这样编写一个Message组件：
```vue
<template>
  <div class="message">
    <p>{{ message }}</p>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup(props) {
    const message = ref(props.message)

    return {
      message
    }
  },
  props: {
    message: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.message {
  /* 你的样式 */
}
</style>
```
在这个组件中，我们使用了Vue3的组合式API。在`setup`函数中，我们创建了一个响应式的`message`，并将它的初始值设置为`props.message`。然后在模板中，我们使用`{{ message }}`来显示这个响应式数据的值。

这种方式的好处是，我们可以在`setup`函数中组织和复用逻辑，使得代码更加清晰和易于维护。  

---

备注：    
prop是什么    
在Vue中，prop（或称为属性）是一种从父组件向子组件传递数据的方式。每个Vue组件都可以声明它自己的props，这些props可以是任何类型的数据，如字符串、数字、对象、数组、布尔值等。

当一个父组件向子组件传递数据时，它会将数据作为HTML属性添加到子组件的标签上，然后子组件可以在其props选项中声明这个属性，以便接收这个数据。

例如，如果我们有一个Message组件，它接收一个名为`message`的prop，那么我们可以这样使用这个组件：  
```vue
<Message message="Hello Vue!"/>
```
然后在Message组件中，我们可以这样声明这个prop：
```vue
export default {
  props: {
    message: {
      type: String,
      required: true
    }
  }
}
```
在这个例子中，`message`就是一个prop，它的值是"Hello Vue!"。

以下是使用Vue3的组合式API来声明props的例子：  
```js
import { toRefs } from 'vue'

export default {
  props: {
    message: {
      type: String,
      required: true
    },
    count: {
      type: Number,
      default: 0
    }
  },
  setup(props) {
    const { message, count } = toRefs(props)

    // 在这里，你可以使用message和count来创建和返回响应式的数据和函数

    return {
      message,
      count
    }
  }
}
```
在这个例子中，我们首先在`props`选项中声明了`message`和`count`两个props。然后在`setup`函数中，我们使用`toRefs`函数将`props`对象转换为一个响应式的对象，然后我们可以直接使用`message`和`count`这两个响应式的引用。  

在选项式API中，我们通过在Vue组件对象中定义一系列选项（如data、methods、computed、watch、props等）来描述组件的行为。这是Vue的经典写法，Vue2和Vue3都支持这种写法。

相比之下，组合式API是Vue3新引入的一种写法，它允许我们使用`setup`函数和一些新的Vue函数（如`ref`、`reactive`、`computed`、`watch`等）来组织和复用逻辑。