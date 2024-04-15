<script>
export default {
    name: 'CharacterCard'
}
</script>

<template>
    <div class="ms-character-card bg-primary">
        Sono la card
    </div>
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

.ms-character-card {
    width: calc((100% / 5) - 12px);
    margin: 6px 6px
}


</style>