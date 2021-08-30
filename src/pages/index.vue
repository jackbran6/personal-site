<template>
  <div class="container">
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Home',
  components: {},

  head: {
    title: 'Hello world!'
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.container {
  column-gap: 3vw;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  row-gap: 3vw;
}

.card {
  border: 2px solid $orange;
  border-radius: 3px;
  height: 30vw;
  width: 100%;
}

@media (max-width: $tablet-max) {
  .container {
    grid-template-columns: 1fr 1fr;
  }
  .card {
    height: 50vw;
  }
}

@media (max-width: $mobile-portrait-max) {
  .container {
    grid-template-columns: 1fr;
  }
  .card {
    height: 100vw;
  }
}
</style>
