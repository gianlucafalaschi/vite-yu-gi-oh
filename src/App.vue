<script>
import AppHeader from './components/AppHeader.vue';
import AppCardsList from './components/AppCardsList.vue';
import CharacterCard from './components/CharacterCard.vue';
 
 export default {
    components: {
      AppHeader,
      AppCardsList,
      CharacterCard,
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
