<script>
import CardsComp from './CardsComp.vue'

export default {
    name: "MainComp",
    components: {
        CardsComp
    },


}

</script>

<template>
    <main class="w-100">
        <div class="container">
            <CardsComp />
        </div>
    </main>
</template>

<style lang="scss">
main {
    background-color: goldenrod;
}
</style>