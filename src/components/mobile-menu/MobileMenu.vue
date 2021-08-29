<template>
  <div class="container">
    <div class="menu" :class="menuOpen && 'menu-open'">
      <nuxt-link to="about" class="menu-item" :class="menuOpen && 'item-open'"
        >about</nuxt-link
      >
      <nuxt-link to="work" class="menu-item" :class="menuOpen && 'item-open'"
        >work</nuxt-link
      >
      <nuxt-link
        to="contact"
        class="menu-item bottom"
        :class="menuOpen && 'item-open'"
        >contact</nuxt-link
      >
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
  background-color: $blue;
  display: flex;
  flex-direction: column;
  height: 0;
  padding-left: 20px;
  padding-right: 20px;
  transition: 0.5s ease-in-out;
  width: 100%;
}
.menu-open {
  height: 100px;
  opacity: 1;
  z-index: 2;
}
.menu-item {
  color: $bright-white;
  opacity: 0;
  transition: 1s ease;
}
.item-open {
  color: $yellow;
  opacity: 1;
}
.bottom {
  padding-bottom: 20px;
}
</style>
