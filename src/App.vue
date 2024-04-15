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
        // Funzione che prende i personaggi dall'API e popola lo store.js
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
          store.characters = response.data.data;
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
