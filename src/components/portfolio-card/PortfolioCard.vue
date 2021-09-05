<template>
  <div class="card">
    <h6 class="title">This is a title</h6>
    <p class="description">
      This is a short description about the project that is being displayed here
    </p>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'PortfolioCard'
})
</script>

<style lang="scss" scoped>
.card {
  border: #000 solid 1px;
  min-width: 300px;
  padding: 2vw;
}
</style>
