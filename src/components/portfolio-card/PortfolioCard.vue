<template>
  <nuxt-link class="link" :to="'portfolio/project/' + link">
    <div class="card">
      <h1 class="title">{{ title }}</h1>
      <p class="description">
        {{ description }}
      </p>
    </div>
  </nuxt-link>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'PortfolioCard',
  props: {
    link: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: 'This is a title'
    },
    description: {
      type: String,
      default:
        'This is a short description about the project that is being displayed here'
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

/* stylelint-disable max-nesting-depth */
.title {
  font-size: 25px;
}
.card {
  border: #000 solid 1px;
  box-shadow: 5px 10px;
  min-height: 150px;
  min-width: 300px;
  padding: 2vw;
  transition: all 0.5s ease;
  &:hover {
    box-shadow: $orange 5px 10px;
  }
}
.image {
  height: 150px;
  width: 300px;
}
.description {
  font-size: 12px;
}
</style>
