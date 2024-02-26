```vue
<script setup>

import { defineProps } from 'vue'

  

// 使用defineProps定义并验证props

const props = defineProps({

  type: {

    type: String, // 指定type属性是字符串类型

    default: 'default', // 默认值为"default"

    validator: (value) => {

      // 验证value是否为指定的几种之一

      return ['primary', 'ghost', 'dashed', 'link', 'text', 'default'].includes(value)

    }

  },

})

</script>

  

<template>

  <button :class="`btn-${props.type}`">Button</button>

</template>
```