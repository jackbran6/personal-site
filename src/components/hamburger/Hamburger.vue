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
  margin-left: 10vw;
  margin-right: 10vw;
  margin-top: 5vw;
}
.hamburger {
  cursor: pointer;
  height: 10px;
  margin: auto;
  transform: rotate(0deg);
  transition: 0.5s ease-in-out;
  width: 40px;
}

.hamburger span {
  background: $dark;
  display: block;
  height: 5px;
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
  top: 10px;
  transform-origin: left center;
}

.hamburger span:nth-child(3) {
  top: 20px;
  transform-origin: left center;
}

.hamburger.open span:nth-child(1) {
  background-color: $red;
  left: 8px;
  top: -3px;
  transform: rotate(45deg);
}

.hamburger.open span:nth-child(2) {
  opacity: 0;
  width: 0%;
}

.hamburger.open span:nth-child(3) {
  background: $red;
  left: 8px;
  top: 25px;
  transform: rotate(-45deg);
}
</style>
