<script>

  import SingleCard from './SingleCardApp.vue';
  import { store } from '../store.js';

  export default {
    data() {
      return {
        store
      }
    },
    components: {
      SingleCard
    }
  }
</script>

<template>

  <div id="main">
    <div class="dropdown">
      <a class="btn dropdown-toggle rounded w-25 mb-4 text-start bg-white" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
        Alien
      </a>
    </div>
    <div class="cards-album bg-white">
      <div class="p-2 bg-black text-white">
        Found X cards 
      </div>
      <div class="cards-container row p-5">
        <div class="single-card col-12 col-sm-6 col-md-3 mb-3 text-center"
             v-for="(card, index) in store.cards"
             :key="index">
             <SingleCard :card="card" />
        </div> 
      </div>
    </div>

  </div>

  
</template>

<style lang="scss" scoped>

</style>
