<script>

export default {
    name: "SingleCardComp",
    props: ['dettagliCard']
}
</script>

<template>
    <div class="card my-3">
        <img :src="dettagliCard.card_images[0].image_url" :alt="dettagliCard.name">
        <h4 class="text-center fw-bold text-white">{{ dettagliCard.name }}</h4>
        <h5 class="text-center text-white">{{ dettagliCard.archetype }}</h5>
    </div>
</template>

<style lang="scss">
.card {
    width: calc(100% / 5 - 10px);
    background-color: goldenrod !important;
    ;
}
</style>