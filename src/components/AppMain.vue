<script>
export default {
    name: 'AppMain',
}

</script>

<template>
    <section class="ms-cards-wrapper">
        <div class="ms-container bg-white my-5">
            <div class="ms-row">row</div>
        </div>
        
    </section>
    
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

.ms-container {
    width: 80%;
    margin: 0 auto;
    padding-left: 10px;
    padding-right: 10px;
}

.ms-row {
    display: flex;
    margin-left: -10px;
    margin-right: -10px;
}

</style>