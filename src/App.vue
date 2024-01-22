<script>

  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    data() {
      return {

      }
    },
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },
    methods: {

    }
  }
</script>

<template>

  <div id="container">

    <AppHeader />
    <AppMain />
    <AppFooter />

  </div>
  
</template>

<style lang="scss">
@use "assets/scss/main.scss" as *;
@import "assets/scss/partials/reset.scss";

</style>
