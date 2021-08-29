<template>
  <div class="container">
    <div class="menu">
      <nuxt-link to="about" class="menu-item">about</nuxt-link>
      <nuxt-link to="work" class="menu-item">work</nuxt-link>
      <nuxt-link to="contact" class="menu-item">contact</nuxt-link>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'NavigationBar'
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.container {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}
.menu-item {
  color: $bright-white;
  padding-left: 20px;
}
</style>
