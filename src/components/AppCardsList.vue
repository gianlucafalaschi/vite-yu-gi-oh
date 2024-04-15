<script>
import { store } from '../store.js';
import CharacterCard from './CharacterCard.vue';

export default {
    name: 'AppMain',

    components: {
        CharacterCard
    },
    data() {
        return{
            store
        };
    }
    
}

</script>

<template>
    <section class="ms-cards-wrapper">
        <div class="ms-container  my-5">
            <div class="ms-row bg-white p-3">
                    <CharacterCard v-for="character in store.characters"></CharacterCard>
            </div>
        </div>
        
    </section>
    
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

.ms-cards-wrapper {
    width: 100%;
}


.ms-container {
    width: 80%;
    margin: 0 auto;
    padding-left: 10px;
    padding-right: 10px;
}

.ms-row {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    margin-left: -10px;
    margin-right: -10px;
    

}


</style>