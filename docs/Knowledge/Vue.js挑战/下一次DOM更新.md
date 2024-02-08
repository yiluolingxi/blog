```vue
<script setup>

import { nextTick, ref } from 'vue';

  

const count = ref(0);

const counter = ref(null);

  

function increment() {

  count.value++;

  nextTick(() => {

    console.log(+counter.value.textContent === 1);// 输出应该为true

  });

  

  /**

   * DOM is not yet updated, how can we make sure that the DOM gets updated

   * Make the output be true

   */

}

</script>

  

<template>

  <button ref="counter" @click="increment">

    {{ count }}

  </button>

</template>
```
