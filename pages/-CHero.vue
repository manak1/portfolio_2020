<template>
  <section class="c-hero">
    <div class="c-hero__wrapper">
      <div class="c-profile">
        <h2 class="c-profile__name profile_text">
          MANAKI<br />
          IKEDA
        </h2>
        <p class="c-profile__position profile_text">
          Frontend Engineer
        </p>
      </div>
      <div id="moon" class="c-parallax">
        <div class="c-parallax__box" data-depth="0.5">
          <img
            src="@/assets/image/hero/moon.svg"
            alt="月の画像"
            class="c-parallax__moon moon"
          />
        </div>

        <div class="c-parallax__box" data-depth="0.6">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star star"
          />
        </div>

        <div class="c-parallax__box" data-depth="1">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star1 star"
          />
        </div>

        <div class="c-parallax__box" data-depth="0.6">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star2 star"
          />
        </div>

        <div class="c-parallax__box" data-depth="0.2">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star3 star"
          />
        </div>

        <div class="c-parallax__box" data-depth="0.8">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star4 star"
          />
        </div>

        <div class="c-parallax__box" data-depth="0.6">
          <img
            src="@/assets/image/hero/hero_star.svg"
            alt=""
            class="c-parallax__star5 star"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Parallax from 'parallax-js'

export default {
  mounted() {
    const scene2 = document.getElementById('moon')

    // eslint-disable-next-line no-unused-vars
    const parallaxInstance = new Parallax(scene2)

    const tl = this.$gsap.timeline({
      repeat: 0,
      ease: this.$gsap.Linear.easeInOut(2)
    })
    tl.from('.star', 1.2, { y: '-100vh', ease: 'back.out(1.7)' }, 2)
    tl.from('.profile_text', 1.5, { x: '-500', ease: 'expo.out' }, 3)
    tl.from('.moon', 2, { x: '500', opacity: '0', ease: 'expo.out' }, 3)
  }
}
</script>

<style lang="scss" scoped>
.c-hero {
  position: relative;
  z-index: 2;

  &__wrapper {
    position: relative;
    display: flex;
    width: 100%;
    height: 100vh;
  }
}

.c-profile {
  position: absolute;
  top: 50%;
  margin-left: 12rem;
  overflow: hidden;
  transform: translateY(-50%);

  &__name {
    @include text-white;

    position: relative;
    font-size: 120px;
    font-weight: bold;
    line-height: 1;

    &::before {
      position: absolute;
      bottom: -16px;
      left: 0;
      display: inline-block;
      width: 88px;
      height: 4px;
      content: '';
      background-color: #fce3a0;
      border-radius: 8px;
    }

    &::after {
      position: absolute;
      bottom: -32px;
      left: 20px;
      display: inline-block;
      width: 88px;
      height: 4px;
      content: '';
      background-color: #fce3a0;
      border-radius: 8px;
    }
  }

  &__position {
    @include text-white;

    margin-top: 56px;
    font-size: 26px;
  }
}

.c-parallax {
  position: absolute;
  top: 25%;
  left: 53%;

  &__box {
    top: -200px !important;
    width: 100%;
    height: 100vh;
  }

  &__star {
    position: absolute;
    top: 430px;
    bottom: -200px;
    left: 500px;
    width: 80px;
    transform: rotate(15deg);
  }

  &__star1 {
    position: relative;
    top: 2%;
    left: -120%;
    height: 180px;
    transform: rotate(-22deg);
  }

  &__star2 {
    position: absolute;
    top: 80%;
    left: -200%;
    width: 120px;
    height: 90px;
    transform: rotate(11deg);
  }

  &__star3 {
    position: relative;
    top: 10%;
    left: -190%;
    height: 60px;
    transform: rotate(141deg);
  }

  &__star4 {
    position: absolute;
    top: 55%;
    left: 10%;
    width: 180px;
    transform: rotate(8deg);
  }

  &__star5 {
    position: relative;
    top: 2%;
    left: 120%;
    height: 130px;
    transform: rotate(3deg);
  }

  &__moon {
    position: relative;
    top: 15%;
    transform: translateY(50%);
  }
}

.c-stars {
  position: absolute;
  width: 1200px;

  &__star {
    position: absolute;
  }

  &__img {
    position: relative;
    top: 80px;
    left: -160px;
    width: 90px;
    transform: rotate(12deg);
  }
}
</style>
