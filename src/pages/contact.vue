<template>
  <div class="container">
    <h1 class="title">contact</h1>
    <div class="contact-container">
      <h1 class="sub-title">email</h1>
      <a href="mailto: jack.branthwaite@gmail.com">
        <p class="link">jack.branthwaite@gmail.com</p></a
      >
    </div>
    <div class="contact-container">
      <h1 class="sub-title">linkedin</h1>
      <a href="https://www.linkedin.com/in/jack-branthwaite/">
        <p class="link">linkedin.com/in/jack-branthwaite</p></a
      >
    </div>
    <div class="contact-container">
      <h1 class="sub-title">github</h1>
      <a href="https://github.com/jackbranthwaite"
        ><p class="link">github.com/jackbranthwaite</p></a
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
.sub-title {
  margin: 0;
}
.contact-container {
  margin-bottom: 2vw;
}
</style>
