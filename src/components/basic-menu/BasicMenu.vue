<template>
  <div>
    <desktop-menu v-if="!mobileView" />
    <mobile-menu v-else />
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import DesktopMenu from '../desktop-menu/DesktopMenu.vue'
import MobileMenu from '../mobile-menu/MobileMenu.vue'

export default Vue.extend({
  name: 'BasicMenu',
  components: { DesktopMenu, MobileMenu },
  data() {
    return {
      menuOpen: false,
      mobileView: false
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
        this.menuOpen = false
      }
    },
    changeMenu() {
      this.menuOpen = !this.menuOpen
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
</style>
