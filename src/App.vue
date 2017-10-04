<template>
  <div id="app">
     <hero></hero>
    <router-view></router-view>
  </div>
</template>

<script>
import Hero from '@/components/Hero'

export default {
  name: 'app',
  components: {
    Hero
  }
}
</script>

<style lang="scss">
@import "./assets/styles/vars";
@import '~bulma';
@import "./assets/styles/main";
</style>
