<template>
  <div id="app">
    <page>
      <card />
    </page>
  </div>
</template>

<script>
import Page from './components/Page.vue'
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Page,
    Card
  }
}
</script>

<style lang="scss">
@import './themes/reset.scss';

#app {
  position: relative;
  width: 100%;
  height: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
