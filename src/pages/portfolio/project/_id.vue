<template>
  <div class="container">
    <h1 class="title">{{}}</h1>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  margin: auto;
  margin-top: 2vw;
  width: 80vw;
}
.card-container {
  display: grid;
  gap: 2vw;
  grid-template-columns: 1fr 1fr 1fr;
  margin-top: 2vw;
}
@include tablet {
  .card-container {
    gap: 4vw;
    grid-template-columns: 1fr 1fr;
  }
}
@include mobile-l {
  .card-container {
    gap: 50px;
    grid-template-columns: 1fr;
  }
}
</style>
