<template>
  <div class="container">
    <nuxt-link class="link" to="portfolio">
      <p class="menu-item">portfolio</p>
    </nuxt-link>
    <nuxt-link class="link" to="about">
      <p class="menu-item">about</p>
    </nuxt-link>
    <nuxt-link class="link" to="contact">
      <p class="menu-item">contact</p>
    </nuxt-link>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'BasicMenu',
  components: {}
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.menu-item {
  color: $black;
  transition: all 0.5s ease;

  &:hover {
    color: $orange;
  }
}
.link {
  text-decoration: none;
}
</style>
