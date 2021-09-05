<template>
  <div class="container">
    <h1 class="title">portfolio</h1>
    <div class="card-container">
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
      <portfolio-card />
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import PortfolioCard from '~/components/portfolio-card/PortfolioCard.vue'

export default Vue.extend({
  name: 'Portfolio',
  components: { PortfolioCard }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  margin: auto;
  width: 80vw;
}
.card-container {
  display: grid;
  gap: 1vw;
  grid-template-columns: 1fr 1fr 1fr;
  margin-top: 2vw;
}
@include tablet {
  .card-container {
    grid-template-columns: 1fr 1fr;
  }
}
@include mobile-l {
  .card-container {
    grid-template-columns: 1fr;
  }
}
</style>
