<template>
  <div class="container">
    <h1 class="title">about</h1>
    <p class="about-text">
      left the coffee industry to complete a one year masters of software
      development<br />now working as a web developer at
      <a class="link" href="https://formfunfunction.com/">form.fun.function</a
      ><br />
      based in wellington, new zealand
    </p>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'About',

  head: {
    title: 'about'
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  margin: auto;
  margin-top: 2vw;
  width: 80vw;
}
.title {
  margin-bottom: 2vw;
}
.link {
  transition: all 0.5s ease;
  &:hover {
    color: $orange;
  }
}
.about-text {
  width: 60vw;
}
</style>
