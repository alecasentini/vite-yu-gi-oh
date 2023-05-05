<script>

export default {
    name: "SingleCardComp",
    props: ['dettagliCard']
}
</script>

<template>
    <div class="card">
        <img :src="dettagliCard.card_images[0].image_url" :alt="dettagliCard.name">
        <h3>{{ dettagliCard.name }}</h3>
        <p>{{ dettagliCard.archetype }}</p>
    </div>
</template>

<style lang="scss">
.card {
    width: calc(100% / 5 - 10px);
}
</style>