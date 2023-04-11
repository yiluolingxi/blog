
TypeScript 与组合式 API” 是指在 Vue.js 中使用 TypeScript 与组合式 API。Vue.js 是一个渐进式的 JavaScript 框架，它支持使用 TypeScript 来编写代码。组合式 API 是 Vue.js 中一种新的编写组件的方式，它提供了更简单、高效和可靠的类型推导。

### Q

-   什么是运行时声明？
-   什么是基于类型的声明？
-   为什么不能同时使用基于类型的声明和运行时声明？
-   如何为 props 声明默认值？
-   如何使用 withDefaults 编译器宏？
-   如何使用 defineComponent() 开启 props 的类型推导？
-   如何使用 defineProps() 的运行时声明？
-   如何使用基于类型的声明对所触发事件的类型进行更细粒度的控制？

-   什么是组合式 API？
-   如何在 Vue 中使用 TypeScript？
-   如何使用 TypeScript 定义 props？
-   如何使用 TypeScript 定义 emits？
-   如何使用 TypeScript 处理原生 DOM 事件？
-   如何使用 provide 和 inject 与 TypeScript？
-   如何使用 TypeScript 访问模板引用？
-   如何使用 TypeScript 定义 setup 函数的返回值？
-   如何使用 TypeScript 定义组件选项？
-   如何使用 TypeScript 定义 computed 属性？
-   如何使用 TypeScript 定义 watch 选项？
-   如何使用 TypeScript 定义生命周期钩子函数？
-   如何使用 TypeScript 定义自定义指令？
-   如何使用 TypeScript 定义自定义组件？
-   如何使用 TypeScript 定义 ref 和 reactive？
-   如何使用 TypeScript 定义 toRefs？
-   如何使用 TypeScript 定义 toRef？
-   如何使用 TypeScript 定义 readonly 和 shallowReadonly？
-   如何使用 TypeScript 定义 unref？
-   如何使用 TypeScript 定义 Teleport？
-   如何使用 TypeScript 定义 Suspense？
-   如何使用 TypeScript 定义自定义渲染函数？
-   如何使用 TypeScript 定义自定义过渡？

请你阅读当前页面的所有内容，并根据当前内容回答我后续的问题, 如果当前页面没有答案，可以到 Vue.js 官方文档中查找。
请问我想学习TypeScript 与组合式 API这个主题时，应该向你提哪些问题？分列表提出
请你回答上面这些问题，分列表回答

###  什么是运行时声明

运行时声明是指传递给 `defineProps()` 的参数会作为运行时的 props 选项使用。例如：

```html
<script setup lang="ts">
  const props = defineProps<{ foo: string; bar?: number }>();
</script>
```

这被称之为“运行时声明”。


### 什么是基于类型的声明

基于类型的声明是指编译器会尽可能地根据类型参数推导出等价的运行时选项。例如：

```html
<script setup lang="ts">
  interface Props {
    foo: string;
    bar?: number;
  }
  const props = defineProps<Props>();
</script>
```

这被称之为“基于类型的声明”。

基于类型的声明和运行时声明都是用来定义 Vue 组件中的 props 的方法。它们的区别在于定义方式不同。

运行时声明是直接在 `defineProps()` 函数中定义 props 的类型，例如：

```html
<script setup lang="ts">
  const props = defineProps<{ foo: string; bar?: number }>();
</script>
```

而基于类型的声明则是先定义一个接口或类型，然后在 `defineProps()` 函数中使用这个接口或类型来定义 props，例如：

```html
<script setup lang="ts">
  interface Props {
    foo: string;
    bar?: number;
  }
  const props = defineProps<Props>();
</script>
```

这两种方法都可以用来定义 props，但不能同时使用。


### 如何为 props 声明默认值

当使用基于类型的声明时，我们失去了为 props 声明默认值的能力。这可以通过 `withDefaults` 编译器宏解决。例如：

```html
<script setup lang="ts">
  interface Props {
    foo: string;
    bar?: number;
  }
  const props = withDefaults(defineProps<Props>(), {
    bar: 0,
  });
</script>
```

这将被编译为等效的运行时 props default 选项。此外，`withDefaults` 帮助程序为默认值提供类型检查，并确保返回的 props 类型删除了已声明默认值的属性的可选标志。


### 什么是 withDefaults 编译器宏

`withDefaults` 是一个编译器宏，用于在使用基于类型的声明时为 props 声明默认值。例如：

```html
<script setup lang="ts">
  interface Props {
    foo: string;
    bar?: number;
  }
  const props = withDefaults(defineProps<Props>(), {
    bar: 0,
  });
</script>
```

这将被编译为等效的运行时 props default 选项。此外，`withDefaults` 帮助程序为默认值提供类型检查，并确保返回的 props 类型删除了已声明默认值的属性的可选标志。


### 什么是 defineExpose

`defineExpose` 是一个函数，用于在 Vue 组件中公开组件实例的方法或属性。例如：

```html
<!-- MyModal.vue -->
<script setup lang="ts">
  import { ref } from 'vue';
  const isContentShown = ref(false);
  const open = () => (isContentShown.value = true);
  defineExpose({ open });
</script>
```

在上面的例子中，我们使用 `defineExpose` 函数公开了 `open` 方法，这样就可以在父组件中通过模板引用来调用这个方法。


### 如何使用 defineComponent() 开启 props 的类型推导

如果没有使用 `<script setup>`，那么为了开启 props 的类型推导，必须使用 `defineComponent()`。传入 `setup()` 的 props 对象类型是从 props 选项中推导而来。例如：

```html
<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    props: {
      foo: String,
      bar: {
        type: Number,
        default: 0,
      },
    },
    setup(props) {
      // `props` 的类型是 `{ foo: string; bar: number }`
    },
  });
</script>
```

在上面的例子中，我们使用 `defineComponent()` 函数定义了一个 Vue 组件，并在其中定义了 props 选项。传入 `setup()` 的 props 对象类型是从 props 选项中推导而来。


### 什么是 InjectionKey 接口


`InjectionKey` 是一个继承自 `Symbol` 的泛型类型，可以用来在提供者和消费者之间同步注入值的类型。例如：

```html
<script setup lang="ts">
  import { provide, inject, InjectionKey } from 'vue';

  const key: InjectionKey<string> = Symbol();

  provide(key, 'foo');

  const value = inject(key);
  // `value` 的类型是 `string | undefined`
</script>
```

在上面的例子中，我们使用 `InjectionKey` 接口定义了一个注入 key，并使用 `provide()` 和 `inject()` 函数来提供和注入值。由于我们使用了 `InjectionKey` 接口，所以注入的值的类型是正确的。  


### 如何使用 InstanceType 工具类型获取组件实例类型

如果你想为一个子组件添加一个模板引用，以便调用它公开的方法，可以使用 TypeScript 内置的 `InstanceType` 工具类型来获取组件实例类型。例如：

```html
<!-- MyModal.vue -->
<script setup lang="ts">
  import { ref } from 'vue';
  const isContentShown = ref(false);
  const open = () => (isContentShown.value = true);
  defineExpose({ open });
</script>

<!-- App.vue -->
<script setup lang="ts">
  import MyModal from './MyModal.vue';
  const modal = ref<InstanceType<typeof MyModal> | null>(null);
  const openModal = () => {
    modal.value?.open();
  };
</script>
```

在上面的例子中，我们首先使用 `typeof` 得到 `MyModal` 组件的类型，然后使用 `InstanceType` 工具类型来获取其实例类型。这样就可以在父组件中通过模板引用来调用子组件公开的方法。


### 如何为 ref 标记类型

可以通过两种方式为 `ref` 标记类型。第一种方式是在定义 `ref` 时显式地指定类型，例如：

```html
<script setup lang="ts">
  import { ref } from 'vue';
  const year: Ref<string | number> = ref('2020');
  year.value = 2020; // 成功！
</script>
```

第二种方式是在调用 `ref()` 函数时使用泛型参数来指定类型，例如：

```html
<script setup lang="ts">
  import { ref } from 'vue';
  const year = ref<string | number>('2020');
  year.value = 2020; // 成功！
</script>
```

这两种方式都可以用来为 `ref` 标记类型。


### 如何为事件处理函数的参数标注类型

在处理原生 DOM 事件时，应该为我们传递给事件处理函数的参数正确地标注类型。例如：

```html
<template>
  <button @click="onClick">Click me</button>
</template>

<script setup lang="ts">
  const onClick = (event: MouseEvent) => {
    console.log(event.clientX);
  };
</script>
```

在上面的例子中，我们为 `onClick` 函数的 `event` 参数显式地标注了 `MouseEvent` 类型。这样就可以在 TypeScript 中正确地使用 `event` 对象的属性和方法。

如果没有类型标注，这个 `event` 参数会隐式地标注为 `any` 类型。这也会在 `tsconfig.json` 中配置了 `"strict": true` 或 `"noImplicitAny": true` 时报出一个 TS 错误。因此，建议显式地为事件处理函数的参数标注类型。


### 如何处理原生 DOM 事件

在处理原生 DOM 事件时，可以在模板中使用 `v-on` 指令（简写为 `@`）来监听事件，并在组件的 `setup` 函数中定义事件处理函数。例如：

```html
<template>
  <button @click="onClick">Click me</button>
</template>

<script setup lang="ts">
  const onClick = (event: MouseEvent) => {
    console.log(event.clientX);
  };
</script>
```

在上面的例子中，我们在模板中使用 `@click` 指令监听了按钮的 `click` 事件，并在 `setup` 函数中定义了 `onClick` 事件处理函数。当用户点击按钮时，就会触发 `onClick` 函数。

此外，在处理原生 DOM 事件时，应该为我们传递给事件处理函数的参数正确地标注类型。这样就可以在 TypeScript 中正确地使用 `event` 对象的属性和方法。


### 什么是 reactive() 的泛型参数

`reactive()` 函数可以接受一个泛型参数来指定返回值的类型。但是，不推荐使用 `reactive()` 的泛型参数，因为处理了深层次 `ref` 解包的返回值与泛型参数的类型不同。例如：

```html
<script setup lang="ts">
  import { reactive } from 'vue';

  // 不推荐！
  const state = reactive<{ foo: string }>({
    foo: 'foo',
  });
</script>
```

在上面的例子中，我们使用了 `reactive()` 的泛型参数来指定返回值的类型。但是，这种用法并不推荐，因为处理了深层次 `ref` 解包的返回值与泛型参数的类型不同。  


### 如何使用 provide 和 inject 同步注入值的类型

`provide` 和 `inject` 函数通常会在不同的组件中运行。要正确地为注入的值标记类型，Vue 提供了一个 `InjectionKey` 接口，它是一个继承自 `Symbol` 的泛型类型，可以用来在提供者和消费者之间同步注入值的类型。例如：

```html
<script setup lang="ts">
  import { provide, inject, InjectionKey } from 'vue';

  const key: InjectionKey<string> = Symbol();

  provide(key, 'foo');

  const value = inject(key);
  // `value` 的类型是 `string | undefined`
</script>
```

在上面的例子中，我们使用 `InjectionKey` 接口定义了一个注入 key，并使用 `provide()` 和 `inject()` 函数来提供和注入值。由于我们使用了 `InjectionKey` 接口，所以注入的值的类型是正确的。


### 如何使用 defineExpose 公开组件实例的方法或属性

`defineExpose` 是一个函数，用于在 Vue 组件中公开组件实例的方法或属性。例如：

```html
<!-- MyModal.vue -->
<script setup lang="ts">
  import { ref } from 'vue';
  const isContentShown = ref(false);
  const open = () => (isContentShown.value = true);
  defineExpose({ open });
</script>
```

在上面的例子中，我们使用 `defineExpose` 函数公开了 `open` 方法，这样就可以在父组件中通过模板引用来调用这个方法。


### 如何使用 defineComponent() 开启 props 的类型推导

如果没有使用 `<script setup>`，那么为了开启 props 的类型推导，必须使用 `defineComponent()`。传入 `setup()` 的 props 对象类型是从 props 选项中推导而来。例如：

```html
<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    props: {
      foo: String,
      bar: {
        type: Number,
        default: 0,
      },
    },
    setup(props) {
      // props 的类型是 { foo: string; bar: number }
    },
  });
</script>
```

在上面的例子中，我们使用 `defineComponent()` 函数定义了一个 Vue 组件，并在其中定义了 props 选项。传入 `setup()` 的 props 对象类型是从 props 选项中推导而来。


### 如何使用 InstanceType 工具类型获取组件实例类型

如果你想为一个子组件添加一个模板引用，以便调用它公开的方法，可以使用 TypeScript 内置的 `InstanceType` 工具类型来获取组件实例类型。例如：

```html
<!-- MyModal.vue -->
<script setup lang="ts">
  import { ref } from 'vue';
  const isContentShown = ref(false);
  const open = () => (isContentShown.value = true);
  defineExpose({ open });
</script>

<!-- App.vue -->
<script setup lang="ts">
  import MyModal from './MyModal.vue';
  const modal = ref<InstanceType<typeof MyModal> | null>(null);
  const openModal = () => {
    modal.value?.open();
  };
</script>
```

在上面的例子中，我们首先使用 `typeof` 得到 `MyModal` 组件的类型，然后使用 `InstanceType` 工具类型来获取其实例类型。这样就可以在父组件中通过模板引用来调用子组件公开的

### 什么是组合式 API

组合式 API 是 Vue 3 中引入的一种新的 API，它提供了一种更灵活的方式来组织组件的逻辑。

### 如何在 Vue 中使用 TypeScript

在 Vue 中使用 TypeScript，您需要在项目中安装 TypeScript 并配置 tsconfig.json 文件。您可以在 Vue 的官方文档中找到关于如何在 Vue 中使用 TypeScript 的详细指南。

### 如何使用 TypeScript 定义 props

当使用 `<script setup>` 时，`defineProps()` 宏支持根据其参数推断 props 类型。这被称为“运行时声明”，因为传递给 `defineProps()` 的参数将被用作运行时的 props 选项。但是，通常更直接地通过泛型类型参数定义 props 是更简单的：`const props = defineProps<{ foo: string; bar?: number }>()`。这被称为“基于类型的声明”。编译器会尽可能地根据类型参数推导出等价的运行时选项。在这种情况下，我们第二个例子中编译出的运行时选项和第一个是完全一致的。您可以使用基于类型的声明或运行时声明，但不能同时使用两者。

### 如何使用 TypeScript 定义 emits

在 `<script setup>` 中，emit 函数也可以使用运行时声明或类型声明进行类型化：`const emit = defineEmits(['change', 'update'])` 或 `const emit = defineEmits<{ (e: 'change', id: number): void; (e: 'update', value: string): void }>()`。类型参数应该是带有调用签名的类型字面量。类型字面量将用作返回的 emit 函数的类型。正如我们所看到的，类型声明使我们能够对触发事件的类型进行更细粒度的控制。

### 如何使用 TypeScript 处理原生 DOM 事件？

在处理原生 DOM 事件时，应该为我们传递给事件处理函数的参数正确地标注类型。例如，如果您在 tsconfig.json 中配置了 “strict”: true 或 “noImplicitAny”: true，则需要显式地为事件处理函数的参数标注类型。此外，您可能需要显式地强制转换 event 上的属性。

### 如何使用 provide 和 inject 与 TypeScript？

provide 和 inject 通常会在不同的组件中运行。要正确地为注入的值标记类型，Vue 提供了一个 InjectionKey 接口，它是一个继承自 Symbol 的泛型类型，可以用来在提供者和消费者之间同步注入值的类型。建议将注入 key 的类型放在一个单独的文件中，这样它就可以被多个组件导入。

### 如何使用 TypeScript 访问模板引用？

有时，您可能需要为一个子组件添加一个模板引用，以便调用它公开的方法。为了获取子组件的类型，我们首先需要通过 typeof 得到其类型，再使用 TypeScript 内置的 InstanceType 工具类型来获取其实例类型。

### 如何使用 TypeScript 定义 setup 函数的返回值？

您可以在 setup 函数中显式地定义返回值的类型。例如：setup(): { count: Ref<number> }。

### 如何使用 TypeScript 定义 Teleport？

Teleport 是 Vue 3 中引入的一种新特性，它允许您将组件的一部分内容传输到 DOM 中的其他位置。您可以在模板中使用 <teleport> 标签来定义 Teleport。目前，Vue 的类型定义不支持 Teleport 的类型检查。
s
###  如何使用 TypeScript 定义 Suspense？ 

Suspense 是 Vue 3 中引入的一种新特性，它允许您定义异步组件加载时的占位内容。您可以在模板中使用 <suspense> 标签来定义 Suspense。目前，Vue 的类型定义不支持 Suspense 的类型检查。

###  如何使用 TypeScript 定义自定义渲染函数？ 

您可以使用 render 函数来定义自定义渲染函数。例如：render() { return h('div', 'Hello World') }。您也可以为 render 函数的参数和返回值显式地定义类型。 

###  如何使用 TypeScript 定义自定义过渡？ 
您可以使用 <transition> 和 <transition-group> 组件来定义自定义过渡。目前，Vue 的类型定义不支持这些组件的类型检查。









