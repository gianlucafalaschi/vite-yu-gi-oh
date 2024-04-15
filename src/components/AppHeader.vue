<script>
export default {
    name: 'AppHeader',
}

</script>

<template>
    <header>
        <div class="container-fluid">
            <div class="row">
                <div class="ms-logo-title-box d-flex align-items-center py-3">
                    <div class="ms-logo-container justify-content-center">
                        <img class="img-fluid" src="../assets/img/1200px-Yu-Gi-Oh!_(Logo).jpg" alt="">
                    </div>
                    <h1 class="my-0">Yu-Gi-Oh Api</h1>
                </div>
                
            </div>
        </div>
        
    </header>
    
</template>

<style scoped lang="scss">
@use'../style/partials/_variables' as *;

header {
    background-color: $brand-primary;
    }

.ms-logo-container {
    
    width: 100px;
}

</style>