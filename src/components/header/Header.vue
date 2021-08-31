<template>
  <div class="header">
    <nuxt-link to="/" class="link">
      <h1 class="name">jack<br />branthwaite</h1>
    </nuxt-link>
    <basic-menu />
  </div>
</template>

<script>
import Vue from 'vue'
import BasicMenu from '../basic-menu/BasicMenu.vue'
export default Vue.extend({
  components: { BasicMenu }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.header {
  display: flex;
  justify-content: space-between;
}

.name {
  color: $black;
  font-size: 6vw;
  line-height: 1.2;
  transition: all 0.5s ease;

  &:hover {
    color: $orange;
  }
}
.link {
  text-decoration: none;
}
</style>
