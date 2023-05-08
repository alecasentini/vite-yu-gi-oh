<script>
import CardsComp from './CardsComp.vue'
import CountCardComp from './CountCardComp.vue';
import SelectArchetypeComp from './SelectArchetypeComp.vue';

export default {
    name: "MainComp",
    components: {
        CardsComp,
        CountCardComp,
        SelectArchetypeComp
    },


}

</script>

<template>
    <main class="w-100 py-5">
        <SelectArchetypeComp />

        <div class="container d-flex flex-column px-0">
            <CountCardComp />
            <CardsComp />
        </div>
    </main>
</template>

<style lang="scss">
main {
    background-color: #d48f38;

    .container {
        border: 50px solid white;
    }
}
</style>