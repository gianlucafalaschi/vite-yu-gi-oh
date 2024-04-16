<script>
    export default {
        name: 'AppFilter'
    }
</script>

<template>
    <section class="filter-box">
        <div class="ms-container">
            <div class="ms-row">
                <div>
                    <select class="select-container" name="" id="">Seleziona un archetype</select>
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
    border: 1px dashed black;
}

.ms-row {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    margin-left: -10px;
    margin-right: -10px;
    border: 1px dashed black;
    

}

</style>