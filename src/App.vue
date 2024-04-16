<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppCardsList from './components/AppCardsList.vue';
import CharacterCard from './components/CharacterCard.vue';
import AppFilter from './components/AppFilter.vue';
 
 export default {
    components: {
      AppHeader,
      AppCardsList,
      CharacterCard,
      AppFilter
    },
    data() {
      return {
        store,
        queryParams: {
          num: 20,
          offset: 0
        }
      };
    },
    methods: {
      getCharactersFromApi() {
        // parametri dell endpoint
        /* const queryParams = {
          num: 20,
          offset: 0
        }; */
        // Funzione che prende i personaggi dall'API e popola lo store.js
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params: this.queryParams
        })
        .then((response) => {
          store.characters = response.data.data;
          console.log(store.characters);
          // popolo lo store con i dati dell'api'
        });
      },
      getArchetypesFromApi() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
        .then((response) => {
          store.archetypes = response.data;
          console.log(store.archetypes);
          // popolo lo store con i dati dell'api'
        });
      } 
    },
    mounted() {
      this.getCharactersFromApi();
      this.getArchetypesFromApi();
    }
  }

</script>

<template>
 <AppHeader></AppHeader>
 <main>
  <AppFilter></AppFilter>
  <AppCardsList></AppCardsList>
 </main>
 

</template>

<style lang="scss">
@use'./style/generic';
</style>
