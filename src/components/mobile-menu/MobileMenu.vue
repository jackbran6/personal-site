<template>
  <div class="container">
    <div class="mobile-menu">
      <hamburger @menuStatus="menuOpen = !menuOpen" />
      <div
        v-if="menuOpen"
        class="mobile-dropdown"
        :class="menuOpen && 'menu-open'"
      >
        <nuxt-link class="link" to="portfolio">
          <p class="mobile-item" :class="menuOpen && 'item-open'">portfolio</p>
        </nuxt-link>
        <nuxt-link class="link" to="about">
          <p class="mobile-item" :class="menuOpen && 'item-open'">about</p>
        </nuxt-link>
        <nuxt-link class="link" to="contact">
          <p class="mobile-item" :class="menuOpen && 'item-open'">contact</p>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import Hamburger from '../hamburger/Hamburger.vue'

export default Vue.extend({
  name: 'MobileMenu',
  components: { Hamburger },
  data() {
    return {
      menuOpen: false,
      mobileView: false
    }
  },
  mounted() {
    this.checkWidth()
    window.addEventListener('resize', this.checkWidth)
  },
  destroyed() {
    window.removeEventListener('reize', this.checkWidth)
  },
  methods: {
    checkWidth() {
      if (window.innerWidth <= 991) {
        this.mobileView = true
      } else if (window.innerWidth > 992) {
        this.mobileView = false
        this.menuOpen = false
      }
    },
    changeMenu() {
      this.menuOpen = !this.menuOpen
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.menu-item {
  color: $black;
  justify-self: flex-end;
  transition: all 0.5s ease;

  &:hover {
    color: $orange;
  }
}
.mobile-item {
  color: $black;
  justify-self: flex-end;
  opacity: 0;
  transition: 1s ease;

  &:hover {
    color: $orange;
  }
}

.item-open {
  opacity: 1;
}

.link {
  text-decoration: none;
}
.mobile-dropdown {
  display: flex;
  flex-direction: column;
  height: 0;
  padding-top: 2vw;
  transition: 2s ease-in-out;
}

.menu-open {
  height: 100px;
  opacity: 1;
  z-index: 2;
}
</style>
