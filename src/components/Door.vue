<template>
  <div class="door-area">
    <div class="door-frame">
      <Gift v-if="open && hasGift" />
    </div>
    <div class="door">
      <div class="number">{{number}}</div>
      <div class="knob"></div>
    </div>
  </div>
</template>

<script>
import Gift from './Gift.vue'

export default {
  name: 'Door',
  components: {Gift},
  props: {
    number: {},
    hasGift: {type: Boolean}
  },
  data(){
    return{
      open: false,
      selected: false
    }
  }
}
</script>

<style>

</style>