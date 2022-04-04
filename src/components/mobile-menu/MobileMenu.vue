<template>
  <div>
    <hamburger @menuStatus="menuOpen = !menuOpen" />

    <div class="mobile-dropdown" :class="menuOpen && 'menu-open'">
      <nuxt-link to="portfolio" class="link">
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

.mobile-item {
  color: $black;
  justify-self: flex-end;
  opacity: 1;
  transition: 1s ease;

  &:hover {
    color: $orange;
  }
}

.link {
  text-decoration: none;
}
.mobile-dropdown {
  animation: growDown 300ms ease-in-out;
  display: none;
  margin-top: 2vw;
  transform-origin: top;
}

@keyframes growDown {
  0% {
    opacity: 0;
    transform: scaleY(0);
  }

  100% {
    opacity: 1;
    transform: scaleY(1);
  }
}

.menu-open {
  align-items: flex-end;
  display: flex;
  flex-direction: column;
  position: absolute;
  right: 1.5rem;
}
</style>
