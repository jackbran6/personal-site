<template>
  <div class="menu-bar" :class="menuOpen && 'menu-open'">
    <div class="container">
      <nuxt-link to="/" style="text-decoration: none">
        <h1 class="name">jack branthwaite</h1>
      </nuxt-link>
      <navigation-bar v-if="!mobileView" />
      <hamburger v-if="mobileView" @menuStatus="menuOpen = !menuOpen" />
    </div>
    <mobile-menu class="mobile-menu" :menu-open="menuOpen" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Hamburger from '../hamburger/Hamburger.vue'
import MobileMenu from '../mobile-menu/MobileMenu.vue'
import NavigationBar from '../navigation-bar/NavigationBar.vue'
export default Vue.extend({
  name: 'MenuBar',
  components: {
    NavigationBar,
    Hamburger,
    MobileMenu
  },
  data() {
    return {
      mobileView: false,
      menuOpen: false
    }
  },
  mounted() {
    this.checkWidth()
    window.addEventListener('resize', this.checkWidth)
  },
  destroyed() {
    window.removeEventListener('reize', this.checkWidth)
  },
  methods: {
    checkWidth() {
      if (window.innerWidth <= 991) {
        this.mobileView = true
      } else if (window.innerWidth > 992) {
        this.mobileView = false
      }
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  align-items: center;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.menu-bar {
  align-items: center;
  background-color: $blue;
  padding: 20px;
}
.menu-open {
  padding-bottom: 20px;
}
h1 {
  margin: 0;
}
.name {
  color: $bright-white;

  :hover {
    color: $yellow;
  }
}
.mobile-menu {
  transition: 1s ease;
}
</style>
