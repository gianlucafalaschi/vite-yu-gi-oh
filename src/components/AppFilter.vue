<script>
import { store } from '../store.js';
    
export default {
    name: 'AppFilter',
    data(){
        return {
            store,
            
        };
    }
}
</script>

<template>
    <section class="filter-box">
        <div class="ms-container">
            <div class="ms-row">
                <div class="select-box">
                    <select v-model="store.selectedArchetype" name="" id="" @change="$emit('searchPerformed')">
                        <option value="">Select Archetype</option>
                        <!-- Scelte disponibili -->
                        <option v-for="archetype in store.archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
                    </select>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">

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
    
    
    .select-box {
        padding: 10px;

        select {
            padding: 4px;
            border-radius: 5px;
        }
    }

}

</style>