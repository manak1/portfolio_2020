<template>
  <header class="l-header">
    <div class="l-header__wrapper">
      <div class="l-box">
        <h1 class="l-box__title">
          MANAKI IKEDA
        </h1>
      </div>
      <div class="l-links">
        <div class="l-sns">
          <a href="https://twitter.com/mikeanakida" class="l-sns__link">
            <img
              src="@/assets/image/header/header_github.svg"
              alt="twitterアイコン"
              class="l-sns__icon"
            />
          </a>

          <a href="https://github.com/manak1" class="l-sns__link">
            <img
              src="@/assets/image/header/header_twitter.svg"
              alt="githubアイコン"
              class="l-sns__icon"
            />
          </a>

          <a href="https://www.wantedly.com/users/80804826" class="l-sns__link">
            Wantedly
          </a>
        </div>
        <div class="l-ham">
          <a href="#" class="l-ham__button">
            <span class="l-ham__line"></span>
            <span class="l-ham__line"></span>
            <span class="l-ham__line"></span>
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.l-header {
  position: absolute;
  z-index: 2000;
  width: 100%;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 2% 5% 0 5%;
  }
}

.l-box {
  &__title {
    font-size: 24px;
    font-weight: normal;
  }
}

.l-sns {
  display: flex;
  align-items: center;

  &__icon {
    width: 28px;
  }

  &__link {
    @include text-white;

    margin: 0 16px;
    font-size: 28px;
  }
}

.l-links {
  display: flex;
}

.l-ham {
  margin-top: -4px;
  margin-left: 20px;

  &__line {
    position: absolute;
    display: inline-block;
    width: 48px;
    height: 3px;
    background-color: #fff;
    transition: 0.3s;

    &:nth-child(2) {
      top: 12px;
      width: 38px;
    }

    &:nth-child(3) {
      top: 24px;
      width: 22px;
    }
  }

  &__button {
    position: relative;
    top: 10px;
    display: inline-block;
    width: 48px;
    height: 100%;

    &:hover {
      opacity: 1;
    }

    &:hover > .l-ham__line {
      width: 48px;
    }
  }
}
</style>
