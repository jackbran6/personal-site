<template>
  <div class="container">
    <nuxt-link to="/" style="text-decoration: none">
      <h1>jack branthwaite</h1>
    </nuxt-link>
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
  margin-left: 10vw;
  margin-right: 10vw;
  margin-top: 5vw;
}
.menu-item {
  padding-left: 20px;
}
h1 {
  margin: 0;
}
</style>
