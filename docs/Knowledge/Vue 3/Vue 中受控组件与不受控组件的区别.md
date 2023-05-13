
在Vue 3中，受控组件和不受控组件是在处理表单元素和组件状态时的两种不同方式。

受控组件（Controlled Components）是指其值受Vue实例的数据绑定控制的组件。组件的值由Vue实例的数据属性提供，并且通过事件将值的更新传递回Vue实例。这种方式下，组件的状态由Vue实例进行管理，组件本身无法修改其值。

不受控组件（Uncontrolled Components）是指其值由组件自身内部状态管理的组件。组件的值存储在组件的内部状态中，并且在需要时可以自由地修改。这种方式下，组件的状态不受Vue实例的直接控制，组件自身负责处理状态的更新。

下面是一个使用组合式API风格的代码示例，展示了受控组件和不受控组件的区别：

```Vue
<template>
  <div>
    <!-- 受控组件 -->
    <input v-model="controlledValue" />

    <!-- 不受控组件 -->
    <input :value="uncontrolledValue" @input="handleUncontrolledInput" />
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    // 受控组件
    const controlledValue = ref('');

    // 不受控组件
    const uncontrolledValue = ref('');

    const handleUncontrolledInput = (event) => {
      uncontrolledValue.value = event.target.value;
    };

    return {
      controlledValue,
      uncontrolledValue,
      handleUncontrolledInput
    };
  }
};
</script>
```

在上面的示例中，`controlledValue`是受控组件的值，它通过`v-model`指令与Vue实例的数据属性进行绑定。当输入框的值发生变化时，`controlledValue`会自动更新，并且这个更新是由Vue实例控制的。

而对于不受控组件，`uncontrolledValue`是组件内部的状态变量，通过`value`属性和`@input`事件进行绑定和更新。当输入框的值发生变化时，`handleUncontrolledInput`方法会更新`uncontrolledValue`的值。这种方式下，组件自身管理状态的更新，不依赖于Vue实例。

总之，受控组件和不受控组件是在处理表单元素和组件状态时的两种不同方式，选择哪种方式取决于具体的需求和开发场景。
