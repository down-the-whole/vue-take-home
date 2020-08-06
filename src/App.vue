<template>
  <div v-if="!isMobile()">
    <div id="container" class="row reverse">
      <div class="col-xs-4">
        <div class="col-xs-12">
          <one v-bind:parentData="firstBlock" />
        </div>
        <div class="col-xs-12">
          <three v-bind:parentData="thirdBlock" />
        </div>
      </div>
      <div class="col-xs-8">
        <div class="col-xs-12">
          <two v-bind:parentData="secondBlock" />
        </div>
      </div>
    </div>
  </div>
  <div v-else>
    <div id="container" class="row">
      <div class="col-xs-12">
        <one v-bind:parentData="firstBlock" />
      </div>
      <div class="col-xs-12">
        <two v-bind:parentData="secondBlock" />
      </div>
      <div class="col-xs-12">
        <three v-bind:parentData="thirdBlock" />
      </div>
    </div>
  </div>
</template>

<script>
import one from './components/one.vue'
import two from './components/two.vue'
import three from './components/three.vue'

import texts from './texts'

const firstBlock = [texts[1], texts[2], texts[3]];
const secondBlock = [texts[4], texts[5], texts[6]];
const thirdBlock = [texts[7], texts[8], texts[9]];

export default {
  name: 'App',
  components: {
    one,
    two,
    three,
  },
  data(){
    return {
      firstBlock: [texts[1], texts[2], texts[3]],
      secondBlock: [texts[4], texts[5], texts[6]],
      thirdBlock: [texts[7], texts[8], texts[9]]
    }
  },
  methods: {
    isMobile() {
      if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        console.log('mobile')
        return true
      } else {
        console.log('no mobile')
        return false
      }
    }
  }
}
</script>
