<template>
    <div id="container">
        <one/>
        <two/>
        <three/>
    </div>
</template>

<script>
import one from './components/one.vue'
import two from './components/two.vue'
import three from './components/three.vue'

import texts from './texts'

export default {
  name: 'App',
  components: {
    one,
    two,
    three,
  }
}
</script>
