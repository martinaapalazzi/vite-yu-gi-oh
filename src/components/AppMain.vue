<script>

  import axios from 'axios';
  import SingleCard from './SingleCardApp.vue';
  import { store } from '../store.js';

  export default {
    data() {
      return {
        store
      }
    },
    components: {
      SingleCard, 
    },
    methods: {
      filteredArchetypes: function() {
        axios
          .get(this.store.baseUrl + '&archetype=' + this.store.searchArchetype)
          .then((response)=> {
            console.log('api response: ', response);
            this.store.cards = response.data.data;
          })
      }
    }
  }
</script>

<template>

  <div id="main">
    <form class="dropdown">
      <select @change="filteredArchetypes" v-model="store.searchArchetype" class="rounded p-2 w-25 mb-4 text-start bg-white" name="" id="">
        <option value="Select archetype">
          Select archetype
        </option>
        <option v-for="(archetype, index) in store.archetypes" :key="index" :value="archetype.archetype_name">
          {{ archetype.archetype_name }}
        </option>
      </select>
    </form>
    <div class="cards-album bg-white">
      <div class="p-2 bg-black text-white">
        Found {{ store.cards.length }} cards
      </div>
      <div class="cards-container row p-5">
        <div class="single-card col-12 col-sm-6 col-md-3  mb-3 text-center"
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
