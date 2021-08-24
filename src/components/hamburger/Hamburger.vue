<template>
  <div class="container">
    <div class="hamburger">
      <span class="menu-line line-one" />
      <span class="menu-line line-two" />
      <span class="menu-line line-three" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Hamburger'
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
}
.menu-line {
  background-color: $dark;
  display: flex;
  height: 2px;
  margin: 2px;
  width: 25px;
}
</style>
