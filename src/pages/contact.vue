<template>
  <div class="container">
    <h1 class="title">contact</h1>
    <div class="contact-container">
      <h1 class="sub-title">email</h1>
      <a href="mailto: jack.branthwaite@gmail.com">
        <span class="link">jack.branthwaite@gmail.com</span></a
      >
    </div>
    <div class="contact-container">
      <h1 class="sub-title">linkedin</h1>
      <a href="https://www.linkedin.com/in/jack-branthwaite/">
        <span class="link">linkedin.com/in/jack-branthwaite</span></a
      >
    </div>
    <div class="contact-container">
      <h1 class="sub-title">github</h1>
      <a href="https://github.com/jackbranthwaite"
        ><span class="link">github.com/jackbranthwaite</span></a
      >
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Contact',

  head: {
    title: 'contact'
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  margin-top: 2vw;
}
.sub-title {
  margin: 0;
}
.contact-container {
  margin-bottom: 2vw;
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
</style>
