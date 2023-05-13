
在Vue 3中，你可以通过创建一个独立的`message`模块来实现一个消息API。下面是一个简单的示例，展示了如何使用Vue 3的Composition API来实现这个功能：

1.  创建一个`message.js`文件，用于定义消息模块。  

```js
import { reactive } from 'vue';

const message = reactive({
  text: '',
  visible: false,
});

function showMessage(text) {
  message.text = text;
  message.visible = true;
}

function hideMessage() {
  message.visible = false;
}

export { message, showMessage, hideMessage };
```

2.  在你的Vue组件中导入并使用`message`模块。  

```Vue
<template>
  <div>
    <button @click="showMessage('Hello')">Show Message</button>
    <div v-if="message.visible">
      {{ message.text }}
      <button @click="hideMessage">Hide Message</button>
    </div>
  </div>
</template>

<script>
import { message, showMessage, hideMessage } from './message';

export default {
  setup() {
    return {
      message,
      showMessage,
      hideMessage,
    };
  },
};
</script>
```

在上面的示例中，`message`对象使用Vue的`reactive`函数来创建一个响应式对象。`showMessage`函数用于显示消息，并将消息内容和可见状态更新到`message`对象中。`hideMessage`函数用于隐藏消息，即将可见状态设置为`false`。在Vue组件中，我们使用`message`对象来显示和隐藏消息，并调用`showMessage`和`hideMessage`函数来更新消息的内容和可见状态。

这只是一个简单的示例，你可以根据需要扩展和定制消息API，例如添加不同类型的消息、设置消息显示时间等。