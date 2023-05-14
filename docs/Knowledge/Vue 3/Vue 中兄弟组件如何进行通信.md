
在 Vue3 中，有多种方法可以实现兄弟组件之间的通信，包括使用 props、事件总线、Vuex 等。下面将分别介绍这几种方法。

### 使用 props

props 是一种父子组件之间进行数据传递的方法，可以通过 prop 在父组件中传递数据，然后在子组件中使用这些数据。在兄弟组件之间进行通信时，可以通过共同的父组件来传递数据，具体步骤如下：

1.  在父组件中声明一个数据属性，例如 `data`。
2.  把 `data` 作为 prop 传递给两个子组件。
3.  在子组件中使用 `props` 接收 `data`。
4.  当一个子组件中的 `data` 发生变化时，通过 `$emit` 方法触发一个自定义事件（例如 `update`），并将变化后的 `data` 作为参数传递给父组件。
5.  父组件中监听子组件的自定义事件，并在事件处理函数中更新 `data`。
6.  当 `data` 发生变化时，Vue 会自动更新两个子组件中使用 `data` 的地方。

使用 props 的优点是简单易懂，适用于简单的数据传递场景，但缺点是不适用于需要频繁更新的场景，因为每次更新都需要通过父组件进行传递。

### 使用事件总线

事件总线是一种全局事件系统，可以在任何组件中触发和监听事件。在兄弟组件之间进行通信时，可以使用一个全局的事件总线来触发和监听事件，具体步骤如下：

1.  创建一个空的 Vue 实例，作为事件总线。
2.  在一个兄弟组件中触发一个自定义事件（例如 `update`），并将需要传递的数据作为参数传递给事件总线。
3.  在另一个兄弟组件中监听这个自定义事件，并在事件处理函数中获取传递的数据。

使用事件总线的优点是可以在任何组件中触发和监听事件，适用于多个组件之间进行通信的场景，但缺点是容易出现命名冲突和事件滥用的问题。

### 使用 Vuex

Vuex 是一个专门为 Vue.js 应用程序开发的状态管理模式。在兄弟组件之间进行通信时，可以通过 Vuex 来管理共享状态，具体步骤如下：

1.  在 Vuex 中声明一个状态（例如 `state`）。
2.  在一个兄弟组件中触发一个自定义事件（例如 `update`），并将需要更新的数据作为参数传递给 Vuex 的 `commit` 方法。
3.  在另一个兄弟组件中使用 Vuex 的 `mapState` 辅助函数获取 `state`。
4.  当 `state` 发生变化时，Vue 会自动更新两个兄弟组件中使用 `state` 的地方。

使用 Vuex 的优点是可以更好地管理共享状态，适用于多个组件之间进行复杂通信的场景，但缺点是增加了状态管理的复杂度。

---

### code demo

### 使用 props 的组合式 API 风格代码

在父组件中声明一个数据属性，并把它作为 prop 传递给两个子组件：  

```js
// Parent.vue
import { defineComponent, ref } from 'vue';
import ChildA from "./ChildA.vue";
import ChildB from "./ChildB.vue";

export default defineComponent({
  components: {
    ChildA,
    ChildB,
  },
  setup() {
    const sharedData = ref("Hello world");
    return { sharedData };
  },
});
```

在子组件中使用 `props` 接收 `data`，并在子组件中使用 `data`：  

```js
// ChildA.vue
import { defineComponent, ref } from 'vue';
export default defineComponent({
  props: {
    data: String,
  },
  setup(props, { emit }) {
    const updateData = () => {
      emit("update", "New data from ChildA");
    };
    return { updateData };
  },
});

// ChildB.vue
import { defineComponent, ref, watch } from 'vue';
export default defineComponent({
  props: {
    data: String,
  },
  setup(props) {
    const data = ref(props.data);
    watch(data, (newValue) => {
      props.$emit("update", newValue);
    });
    return { data };
  },
});

```

当一个子组件中的 `data` 发生变化时，通过 `$emit` 方法触发一个自定义事件（例如 `update`），并将变化后的 `data` 作为参数传递给父组件。父组件中监听子组件的自定义事件，并在事件处理函数中更新 `data`。当 `data` 发生变化时，Vue 会自动更新两个子组件中使用 `data` 的地方。

### 使用事件总线的组合式 API 风格代码

创建一个空的 Vue 实例，并在一个兄弟组件中触发一个自定义事件（例如 `update`），并将需要传递的数据作为参数传递给事件总线：  

```js
// ChildA.vue
import { defineComponent, inject } from 'vue';
export default defineComponent({
  setup() {
    const root = inject("root");
    const updateData = () => {
      root.$emit("update", "New data from ChildA");
    };
    return { updateData };
  },
});

// ChildB.vue
import { defineComponent, inject, ref, watch } from 'vue';
export default defineComponent({
  setup() {
    const root = inject("root");
    const data = ref("");
    watch(data, (newValue) => {
      root.$emit("update", newValue);
    });
    return { data };
  },
});
```

在根组件中创建一个空的 Vue 实例，并将其注入到子组件中：  

```js
// App.vue
import { createApp } from 'vue';
import Parent from "./Parent.vue";

const app = createApp(Parent);
const root = app._context;
app.provide("root", root);
app.mount("#app");

```

在另一个兄弟组件中监听这个自定义事件，并在事件处理函数中获取传递的数据。

### 使用 Vuex 的组合式 API 风格代码

在 Vuex 中声明一个状态（例如 `state`）：  

```js
// store.js
import { createStore } from 'vuex';

const store = createStore({
  state() {
    return {
      sharedData: "Hello world",
    };
  },
  mutations: {
    updateData(state, data) {
      state.sharedData = data;
    },
  },
});

export default store;

```

在一个兄弟组件中触发一个自定义事件（例如 `update`），并将需要更新的数据作为参数传递给 Vuex 的 `commit` 方法：  

```js
// ChildA.vue
import { defineComponent, useStore } from 'vuex';
export default defineComponent({
  setup() {
    const store = useStore();
    const updateData = () => {
      store.commit("updateData", "New data from ChildA");
    };
    return { updateData };
  },
});

// ChildB.vue
import { defineComponent, useStore, computed } from 'vue';
export default defineComponent({
  setup() {
    const store = useStore();
    const data = computed(() => store.state.sharedData);
    return { data };
  },
});

```

当 `state` 发生变化时，Vue 会自动更新两个兄弟组件中使用 `state` 的地方。