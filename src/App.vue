<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppCardsList from './components/AppCardsList.vue';
import CharacterCard from './components/CharacterCard.vue';
 
 export default {
    components: {
      AppHeader,
      AppCardsList,
      CharacterCard,
    },
    data() {
      return {
        store
      };
    },
    methods: {
      getCharactersFromApi() {
        // parametri dell endpoint
        const queryParams = {
          num: 20,
          offset: 0
        };
        // Funzione che prende i personaggi dall'API e popola lo store.js
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params: queryParams
        })
        .then((response) => {
          store.characters = response.data.data;
          // popolo lo store con i dati dell'api'
        });
      }
    },
    mounted() {
      this.getCharactersFromApi();
    }
  }

</script>

<template>
 <AppHeader></AppHeader>
 <main>
  <AppCardsList></AppCardsList>
 </main>
 

</template>

<style lang="scss">
@use'./style/generic';
</style>
