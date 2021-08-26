<template>
  <div class="door-area">

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