<script>

  import AppHeader from "./components/AppHeader.vue"
  import AppMain from "./components/AppMain.vue"
  import AppFooter from "./components/AppFooter.vue"
  import axios from 'axios';
  import { store } from './store.js';

  export default {
    data() {
      return {
        store
      }
    },
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },
    methods: {
      getResponse: function (){
        axios.get(this.store.baseUrl, {
            params: {
              archetype: this.searchArchetype
            }
          })
          .then((response) => {
            console.log('api response: ', response);
            this.store.cards = response.data.data;
            console.log(this.store.cards);
          })
          .catch((error) => {
            this.store.cards = [];
          })
      }
    },
    mounted() {
      this.getResponse()
    },
  }
</script>

<template>

  <AppHeader />

  <AppMain @performSearch="getResponse()" />

  <AppFooter />

</template>

<style lang="scss">
@use "assets/scss/main.scss" as *;
@import "assets/scss/partials/reset.scss";

</style>
