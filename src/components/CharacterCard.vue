<script>
export default {
    name: 'CharacterCard'
}
</script>

<template>
    <div class="ms-character-card">
        <div class="ms-imagine-container mb-2">
            <img class="img-fluid" src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt="">
        </div>
        <div class="ms-name-container mb-2">
            <h5 class="mb-0">\"A\" Cell Breeding Device</h5>
        </div>
        <div class="ms-archetype-container mb-2">
            <h6 class="mb-0">Alien</h6>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

.ms-character-card {
    width: calc((100% / 5) - 12px);
    margin: 6px 6px;
    background-color: $brand-primary;

    .ms-name-container {
        color: white;
        text-wrap: wrap;
        text-align: center;
    }
    .ms-archetype-container {
        color: black;
        font-weight: normal;
        text-align: center;
    }
}


</style>