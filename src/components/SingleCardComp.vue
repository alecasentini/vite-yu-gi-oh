<script>

export default {
    name: "SingleCardComp",
    props: ['dettagliCard']
}
</script>

<template>
    <div class="card mb-3">
        <img :src="dettagliCard.card_images[0].image_url" :alt="dettagliCard.name">
        <h4 class="text-center fw-bold text-white p-2">{{ dettagliCard.name }}</h4>
        <h5 class="text-center text-white p-2">{{ dettagliCard.archetype }}</h5>
    </div>
</template>

<style lang="scss">
.card {
    width: calc(100% / 5 - 10px);
    background-color: #d48f38 !important;
    border: 0 !important;
}
</style>