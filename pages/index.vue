<template>
  <client-only>
    <full-page :options="options">
      <div></div>
    </full-page>
  </client-only>
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
        onLeave: this.onMove,
        easingcss3: 'cubic-bezier(0.77, 0.2, 0.05, 1)'
      }
    }
  }
}
</script>
