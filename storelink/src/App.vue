<template>
  <div id="app">
    <Navigation />
    <router-view/>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation'
export default {
  components: {
    Navigation
  }
}
</script>

<style lang="scss">
  @import './assets/styles/reset.css';
  @import './assets/styles/variables.scss';
  @import './assets/styles/styles.scss';
</style>
