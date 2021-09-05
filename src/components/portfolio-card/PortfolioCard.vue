<template>
  <nuxt-link class="link" :to="link">
    <div class="card">
      <h6 class="title">{{ title }}</h6>
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
  transition: all 0.5s ease;
}
.card {
  border: #000 solid 1px;
  box-shadow: 5px 10px;
  min-width: 300px;
  padding: 2vw;

  &:hover {
    .title {
      color: $orange;
    }
  }
}
</style>
