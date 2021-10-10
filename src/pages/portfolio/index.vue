<template>
  <div class="container">
    <h1 class="title">portfolio</h1>
    <div class="card-container">
      <portfolio-card
        title="Todo List Website"
        description="A simple todo list application built in Vanilla JavaScript. Based on a tutorial found on YouTube"
      />
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
