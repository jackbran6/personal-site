<template>
  <header class="header">
    <menu-bar class="menu" />
  </header>
</template>

<style lang="scss" scoped>
@import '~assets/styles/config';

.header {
  @include type(14px, 18px);

  display: grid;
}
.menu {
  position: fixed;
  width: 96vw;
}
</style>
