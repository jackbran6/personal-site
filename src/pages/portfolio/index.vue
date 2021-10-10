<template>
  <div class="container">
    <h1 class="title">portfolio</h1>
    <div class="card-container">
      <portfolio-card
        title="Photography Website"
        description="Personal photography website built in HTML, CSS, JavaScript, and PHP for  a university project"
        link="1"
      />
      <portfolio-card
        title="Workplace Employee Site"
        description="Group unversity project built with the MERN stack. "
        link="2"
      />
      <portfolio-card
        title="Android Web Browser"
        description="Web browser built in Java for a university project"
        link="3"
      />
      <portfolio-card
        title="Android Todo List"
        description="Todo list application built in Java for a university project"
        link="4"
      />
      <portfolio-card
        title="iOS Todo List"
        description="Todo list application built in Swift for a university project"
        link="5"
      />
      <portfolio-card
        title="Todo List Website"
        description="A simple todo list application built in Vanilla JavaScript. Based on a tutorial found on YouTube"
        link="6"
      />
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
