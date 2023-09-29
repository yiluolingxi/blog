在Vue中，`v-for`的优先级高于`v-if`。这意味着如果一个元素同时包含`v-if`和`v-for`，那么`v-for`会先执行。

然而，Vue官方建议尽量避免在同一个元素上同时使用`v-if`和`v-for`，因为这可能导致性能问题。在大多数情况下，你可以使用计算属性来替代这种用法，预先过滤出需要渲染的列表项。

在Vue中，`v-for`的优先级高于`v-if`。这意味着如果一个元素同时包含`v-if`和`v-for`，那么`v-for`会先执行。以下是一个简单的示例：  
```HTML
<template>
  <div>
    <!-- v-for has higher priority than v-if -->
    <div v-for="item in list" :key="item.id" v-if="item.isActive">
      {{ item.name }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        { id: 1, name: 'Item 1', isActive: true },
        { id: 2, name: 'Item 2', isActive: false },
        { id: 3, name: 'Item 3', isActive: true },
      ]
    }
  }
}
</script>
```
在这个示例中，`v-for`会先执行，遍历`list`中的每个元素。然后，对于每个元素，`v-if`会检查`isActive`属性，只有当`isActive`为`true`时，才会渲染对应的元素。

然而，Vue官方建议尽量避免在同一个元素上同时使用`v-if`和`v-for`，因为这可能导致性能问题。在大多数情况下，你可以使用计算属性来替代这种用法，预先过滤出需要渲染的列表项。  

在Vue 3中，如果你使用组合式API，你可以使用`reactive`或`ref`来创建响应式数据，使用`computed`来创建计算属性。以下是一个简单的示例：  
```HTML
<template>
  <div>
    <!-- v-for has higher priority than v-if -->
    <div v-for="item in activeList" :key="item.id">
      { item.name }
    </div>
  </div>
</template>

<script>
import { reactive, computed } from 'vue'

export default {
  setup() {
    const state = reactive({
      list: [
        { id: 1, name: 'Item 1', isActive: true },
        { id: 2, name: 'Item 2', isActive: false },
        { id: 3, name: 'Item 3', isActive: true },
      ]
    })

    const activeList = computed(() => {
      return state.list.filter(item => item.isActive)
    })

    return {
      activeList
    }
  }
}
</script>
```
在这个示例中，我们使用`reactive`创建了一个响应式对象`state`，并在其中定义了`list`。然后，我们使用`computed`创建了一个计算属性`activeList`，它返回`list`中`isActive`为`true`的元素。在模板中，我们使用`v-for`来遍历`activeList`，渲染每个活动的元素。