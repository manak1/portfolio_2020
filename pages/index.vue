<template>
  <full-page id="fullpage" :options="options">
    <div class="section fp-table active">
      <div class="fp-tableCell">
        <h3>Section 1</h3>
      </div>
    </div>
    <div class="section">
      ...
    </div>
  </full-page>
</template>

<script>
export default {
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
