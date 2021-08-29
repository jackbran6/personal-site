<template>
  <div class="container">
    <div class="hamburger" :class="menuOpen && 'open'" @click="menuClicked">
      <span />
      <span />
      <span />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Hamburger',

  data() {
    return {
      menuOpen: false
    }
  },
  methods: {
    menuClicked() {
      this.menuOpen = !this.menuOpen
      this.$emit('menuStatus')
      console.log(this.menuOpen)
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  display: flex;
  justify-content: flex-end;
}
.hamburger {
  cursor: pointer;
  height: 10px;
  margin-top: 5px;
  transform: rotate(0deg);
  transition: 0.5s ease-in-out;
  width: 30px;
}

.hamburger span {
  background: $bright-white;
  display: block;
  height: 2px;
  left: 0;
  opacity: 1;
  position: absolute;
  transform: rotate(0deg);
  transition: 0.25s ease-in-out;
  width: 100%;
}
.hamburger span:nth-child(1) {
  top: 0;
  transform-origin: left center;
}

.hamburger span:nth-child(2) {
  margin-left: 3px;
  top: 4px;
  transform-origin: left center;
}

.hamburger span:nth-child(3) {
  top: 8px;
  transform-origin: left center;
}

.hamburger.open span:nth-child(1) {
  background-color: $orange;
  left: 8px;
  top: -6px;
  transform: rotate(45deg);
}

.hamburger.open span:nth-child(2) {
  opacity: 0;
  width: 0%;
}

.hamburger.open span:nth-child(3) {
  background: $orange;
  left: 8px;
  top: 15px;
  transform: rotate(-45deg);
}
</style>
