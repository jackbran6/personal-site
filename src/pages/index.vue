<template>
  <div class="container"></div>
</template>
<script lang="ts">
import Vue from 'vue'
import Intro from '@/components/intro/Intro.vue'
import Code from '@/components/intro/Code.vue'
import Heading from '@/components/intro/Heading.vue'

export default Vue.extend({
  name: 'Home',
  components: {
    Intro,
    Code,
    Heading
  },

  head: {
    title: 'Hello world!'
  }
})
</script>
