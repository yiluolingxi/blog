```vue
<script setup lang="ts">

import { shallowRef, watch } from "vue"

  

const state = shallowRef({ count: 1 })

  

// Does NOT trigger

watch(state, () => {

  console.log("State.count Updated")

}, { deep: true })

  

/**

 * Modify the code so that we can make the watch callback trigger.

*/

state.value = 2

  

</script>

  

<template>

  <div>

    <p>

      {{ state.count }}

    </p>

  </div>

</template>
```
