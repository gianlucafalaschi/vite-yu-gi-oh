<script>
export default {
    name: 'CharacterCard',
    /* CharacterCard accetta un oggetto che chiamo characterInfo */
    props: {
        characterInfo: Object
    }
}
</script>

<template>
    <div class="ms-character-card">
        <div class="ms-imagine-container mb-2">
            <img class="img-fluid" :src="characterInfo.card_images[0].image_url_small">
        </div>
        <div class="ms-name-container mb-2">
            <h5 class="mb-0">{{characterInfo.name}}</h5>
        </div>
        <div class="ms-archetype-container mb-2">
            <h6 class="mb-0">{{characterInfo.archetype}}</h6>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

.ms-character-card {
    width: 100%;
    margin: 6px 6px;
    background-color: $brand-primary;

    .ms-imagine-container {
        width: 100%;
        display: flex;
        justify-content: center;

    }
    .ms-name-container {
        width: 100%;
        color: white;
        text-wrap: wrap;
        text-align: center;
        word-break: break-all;
    }
    .ms-archetype-container {
        color: black;
        font-weight: normal;
        text-align: center;
    }
}

/* MEDIA QUERIES */

/*----------------
    COLUMNS per XS > 0px
-----------------*/


/*----------------
    COLUMNS per SM >= 576px
-----------------*/
@media screen and (min-width: 576px) {

    .ms-character-card {
        width: calc((100% / 4) - 12px);
    }

}

/*----------------
COLUMNS per MD >= 768px
-----------------*/

/*----------------
COLUMNS per LG >= 992px
-----------------*/
@media screen and (min-width: 992px) {

    .ms-character-card {
        width: calc((100% / 5) - 12px );
    }

}

</style>