<template>
  <div id="app">
    <hero></hero>
    <router-view></router-view>
    <the-footer></the-footer>
  </div>
</template>

<script>
import Hero from '@/components/Hero'
import TheFooter from '@/components/TheFooter'

export default {
  name: 'app',
  components: {
    Hero,
    TheFooter
  }
}
</script>

<style lang="scss">
@import "./assets/styles/vars";
@import '~bulma';
@import "./assets/styles/main";
</style>
