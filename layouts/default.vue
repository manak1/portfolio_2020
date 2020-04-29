<template>
  <div>
    <div class="c-loader"></div>
    <div>
      <l-header />
      <nuxt />
    </div>
    <div id="background" class="c-background">
      <img
        src="@/assets/image/background.svg"
        class="c-background__img"
        data-depth="0.2"
        alt="月の光"
      />
    </div>
  </div>
</template>

<script>
import Parallax from 'parallax-js'
import LHeader from '@/components/Layout/LHeader'
export default {
  components: {
    LHeader
  },
  mounted() {
    const scene = document.getElementById('background')
    // eslint-disable-next-line no-unused-vars
    const parallaxInstance = new Parallax(scene)

    const tl = this.$gsap.timeline({
      repeat: 0,
      ease: this.$gsap.Linear.easeInOut(2)
    })
    tl.to('.c-loader', 1.2, { y: '-100vh', ease: 'expo.out' }, 1)
  }
}
</script>

<style lang="scss" scoped>
.c-background {
  position: fixed;
  top: -150px;
  left: 35%;
  z-index: 1;
  width: 1300px;

  &__img {
    width: 1200px;
  }
}

.c-loader {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 2000;
  background-color: #020b16;
}
</style>
