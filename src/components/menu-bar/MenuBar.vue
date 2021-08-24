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
      mobileView: true
    }
  },
  created() {
    this.handleView()
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 990
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
</style>
