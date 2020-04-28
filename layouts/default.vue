<template>
  <div>
    <div>
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
export default {
  mounted() {
    const scene = document.getElementById('background')
    // eslint-disable-next-line no-unused-vars
    const parallaxInstance = new Parallax(scene)
  }
}
</script>

<style lang="scss" scoped>
.c-background {
  position: fixed;
  top: -100px;
  left: 35%;
  z-index: 1;
  width: 1300px;

  &__img {
    width: 1200px;
  }
}
</style>
