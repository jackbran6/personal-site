<template>
  <div class="container">
    <h1>jack branthwaite</h1>
    <div class="menu">
      <nuxt-link to="about" class="menu-item">about</nuxt-link>
      <nuxt-link to="work" class="menu-item">work</nuxt-link>
      <nuxt-link to="contact" class="menu-item">contact</nuxt-link>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  justify-self: center;
  margin-top: 50px;
  width: 80vw;
}
.menu {
  align-self: flex-end;
  display: flex;
  flex-direction: row;
  width: 40vw;
}
.menu-item {
  padding-right: 20px;
}
h1 {
  margin: 0;
}
</style>
