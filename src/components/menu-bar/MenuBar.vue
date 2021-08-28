<template>
  <div class="container">
    <navigation-bar v-if="!mobileView" />
    <hamburger v-if="mobileView" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Hamburger from '../hamburger/Hamburger.vue'
import NavigationBar from '../navigation-bar/NavigationBar.vue'
export default Vue.extend({
  name: 'MenuBar',
  components: {
    NavigationBar,
    Hamburger
  },
  data() {
    return {
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
      }
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
</style>
