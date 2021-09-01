<template>
  <div class="container">
    <div v-if="!mobileView" class="main-menu">
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
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DesktopMenu',
  components: {},
  data() {
    return {
      menuOpen: false,
      mobileView: false
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.menu-item {
  color: $black;
  justify-self: flex-end;
  transition: all 0.5s ease;

  &:hover {
    color: $orange;
  }
}
.mobile-item {
  color: $black;
  justify-self: flex-end;
  opacity: 0;
  transition: 1s ease;

  &:hover {
    color: $orange;
  }
}

.item-open {
  opacity: 1;
}

.link {
  text-decoration: none;
}
.mobile-dropdown {
  display: flex;
  flex-direction: column;
  height: 0;
  padding-top: 2vw;
  transition: 2s ease-in-out;
}

.menu-open {
  height: 100px;
  opacity: 1;
  z-index: 2;
}
</style>
