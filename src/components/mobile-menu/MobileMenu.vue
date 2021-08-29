<template>
  <div class="container">
    <div class="menu" :class="menuOpen && 'menu-open'">
      <nuxt-link to="about" class="menu-item">about</nuxt-link>
      <nuxt-link to="work" class="menu-item">work</nuxt-link>
      <nuxt-link to="contact" class="menu-item">contact</nuxt-link>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'MobileMenu',
  props: {
    menuOpen: {
      type: Boolean,
      default: false
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.menu {
  display: flex;
  flex-direction: column;
  height: 0;
  opacity: 0;
  transition: 0.5s ease-in-out;
}
.menu-open {
  height: 100%;
  opacity: 1;
  z-index: 2;
}
.menu-item {
  color: $bright-white;
}
</style>
