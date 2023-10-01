Vue 3中组件之间的通信方式主要有以下几种：

1. **Props / Emit**：这是父子组件之间最常用的通信方式。父组件通过props向子组件传递数据，子组件通过emit给父组件发送消息。
    
2. **Provide / Inject**：这是一种允许我们在任何级别的组件中注入依赖项的方式。祖先组件有一个方法provide来提供变量，然后其后代组件可以通过inject来接收这个变量。
    
3. **Vuex**：Vuex是一个专为Vue.js应用程序开发的状态管理模式。它采用集中式存储管理应用的所有组件的状态，并以相应的规则保证状态以一种可预测的方式发生变化。这是一个全局通信方式，适合大型应用。
    
4. **Teleport**：Vue 3引入了新的Teleport组件，它允许我们将子组件渲染到DOM的其他位置，这为组件通信提供了新的可能性。
    
5. **Composition API**：Vue 3的新Composition API也为组件通信提供了新的方式。我们可以通过创建可复用的composable函数来共享逻辑和状态，这些函数可以在任何组件中使用。
    

以上就是Vue 3中组件之间的主要通信方式，具体使用哪种方式，需要根据实际的需求和场景来决定。  

1. **Props / Emit**：    
在Composition API中，props是作为setup函数的第一个参数传入的，而emit则是作为setup函数的第二个参数的一个属性传入的。

以下是一个使用Composition API的组件示例，该组件接收一个prop并触发一个事件：
```js
<template>
  <button @click="emitEvent">{ myProp }</button>
</template>

<script>
export default {
  props: ['myProp'],
  setup(props, { emit }) {
    const emitEvent = () => {
      emit('myEvent', 'Hello, Parent!')
    }

    return {
      emitEvent
    }
  }
}
</script>
```
在这个例子中，我们在setup函数中定义了一个方法emitEvent，当按钮被点击时，这个方法会被调用，从而触发一个名为'myEvent'的事件，并传递一个消息给父组件。 

在Vue 3的Composition API中，你可以通过以下方式使用Props和Emit实现父子组件之间的通信：

1. **Props**：在子组件中，你可以通过`props`参数接收从父组件传递过来的数据。`props`是`setup`函数的第一个参数。
    
2. **Emit**：在子组件中，你可以通过`context.emit`来触发一个自定义事件，然后在父组件中监听这个事件。`context`是`setup`函数的第二个参数。
    

以下是一个示例：  
```js
// 父组件
<template>
  <child-component :myProp="parentData" @childEvent="handleEvent"></child-component>
</template>

<script>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

export default {
  components: {
    ChildComponent
  },
  setup() {
    const parentData = ref('Hello, Child!')

    const handleEvent = (payload) => {
      console.log(payload)
    }

    return {
      parentData,
      handleEvent
    }
  }
}
</script>

// 子组件
<template>
  <div>
    <p>{ myProp }</p>
    <button @click="emitEvent">Click me</button>
  </div>
</template>

<script>
import { ref, toRefs } from 'vue'

export default {
  props: ['myProp'],
  setup(props, context) {
    const { myProp } = toRefs(props)

    const emitEvent = () => {
      context.emit('childEvent', 'Hello, Parent!')
    }

    return {
      myProp,
      emitEvent
    }
  }
}
</script>
```
在这个例子中，父组件通过`props`向子组件传递数据，子组件通过`emit`给父组件发送消息。

2. **Provide / Inject**： 
在Vue 3的Composition API中，你可以通过以下方式使用Provide和Inject实现组件之间的通信：

1. **Provide**：在祖先组件中，你可以使用`provide`函数来提供一个值。这个值可以是任何类型，包括响应式的值。
    
2. **Inject**：在后代组件中，你可以使用`inject`函数来接收祖先组件提供的值。
    

以下是一个示例：  
```js
// 祖先组件
<script>
import { provide, ref } from 'vue'

export default {
  setup() {
    const forChild = ref('Hello, Child!')
    provide('forChild', forChild)

    return {}
  }
}
</script>

// 后代组件
<script>
import { inject } from 'vue'

export default {
  setup() {
    const forChild = inject('forChild')
    console.log(forChild.value) // 输出 "Hello, Child!"

    return {}
  }
}
</script>
```
在这个例子中，祖先组件使用`provide`函数来提供一个响应式的值，然后在后代组件中使用`inject`函数来接收这个值。  

3. **Vuex**：
如果你想使用Vue 3的Composition API和Vuex 4来实现同样的功能,可以使用`useStore`函数来获取Vuex的store，然后使用`computed`函数来创建响应式的计算属性。以下是一个示例：  
```js
// store.js
import { createStore } from 'vuex'

export default createStore({
  state: {
    message: 'Hello, World!'
  },
  mutations: {
    setMessage(state, payload) {
      state.message = payload
    }
  }
})

// 组件
<template>
  <div>{ messageFromStore }</div>
</template>

<script>
import { computed } from 'vue'
import { useStore } from 'vuex'

export default {
  setup() {
    const store = useStore()
    const messageFromStore = computed(() => store.state.message)

    return {
      messageFromStore
    }
  }
}
</script>
```
在这个例子中，我们使用`useStore`函数来获取store，然后使用`computed`函数来创建一个响应式的计算属性。这样，当store中的`message`状态改变时，组件中的`messageFromStore`也会自动更新。

此外，你也可以在`setup`函数中调用store的`commit`或`dispatch`方法来触发mutation或action，从而改变状态。例如：  
```js
<script>
import { useStore } from 'vuex'

export default {
  setup() {
    const store = useStore()

    const setMessage = (newMessage) => {
      store.commit('setMessage', newMessage)
    }

    return {
      setMessage
    }
  }
}
</script>
```
在这个例子中，我们定义了一个`setMessage`方法，当这个方法被调用时，它会触发`setMessage` mutation，从而改变store中的`message`状态。  

4. **Teleport**：
```js
// 父组件
<template>
  <div>
    <teleport to="#end">
      <p>{ message }</p>
    </teleport>
  </div>
  <div id="end"></div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const message = ref('Hello, Teleport!')

    return {
      message
    }
  }
}
</script>
```
在这个例子中，我们使用`setup`函数和`ref`函数来创建一个响应式的数据源`message`。然后在模板中，我们使用Teleport将一个`<p>`元素渲染到`#end`元素中。  

5. Composition API是Vue 3引入的一种新的API，它提供了一种更灵活的方式来组织和复用组件的逻辑。

在Vue 2中，我们通常会使用mixins或者scoped slots来复用组件的逻辑，但这些方法都有一些缺点，比如命名冲突、不清晰的来源等。而Composition API通过使用函数来组织和复用逻辑，解决了这些问题。

一个composable函数就是一个可以被复用的函数，它可以包含一些响应式的数据和方法。这个函数可以在任何组件的`setup`函数中调用，从而在这个组件中使用这个函数中的数据和方法。

例如，我们可以创建一个用于获取和更新用户信息的composable函数：  
```js
import { ref } from 'vue'
import { getUser, updateUser } from '@/api/user'

export function useUser() {
  const user = ref(null)

  const fetchUser = async (id) => {
    user.value = await getUser(id)
  }

  const saveUser = async () => {
    await updateUser(user.value)
  }

  return {
    user,
    fetchUser,
    saveUser
  }
}
```
然后在任何组件中，我们都可以使用这个函数：  
```js
import { useUser } from '@/composables/useUser'

export default {
  setup() {
    const { user, fetchUser, saveUser } = useUser()

    // 在这个组件中，我们可以使用`user`、`fetchUser`和`saveUser`

    return {
      user,
      fetchUser,
      saveUser
    }
  }
}
```
这样，我们就可以在多个组件中复用获取和更新用户信息的逻辑，而不需要在每个组件中都重复这段逻辑。