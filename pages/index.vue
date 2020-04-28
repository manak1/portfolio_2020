<template>
  <client-only>
    <full-page id="fullpage" class="p-fullpage" :options="options">
      <div class="section fp-table active">
        <div class="fp-tableCell">
          <c-hero />
        </div>
      </div>
      <div class="section">
        ...
      </div>
    </full-page>
  </client-only>
</template>

<script>
import CHero from '@/pages/-CHero'
export default {
  components: {
    CHero
  },
  data() {
    return {
      options: {
        licenseKey: 'YOUR_KEY_HERE',
        menu: '#menu',
        anchors: ['page1', 'page2', 'page3'],
        scrollingSpeed: 800,
        afterLoad: this.afterLoad,
        animateAnchor: true,
        navigation: true,
        navigationPosition: 'left',
        easingcss3: 'cubic-bezier(0.77, 0.2, 0.05, 1)'
      }
    }
  }
}
</script>

<style lang="scss">
html,
body {
  background-color: #071e3b;
}

.p-fullpage {
  z-index: 999;
}
</style>
