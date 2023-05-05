<script>
import { store } from '../store'
import SingleCardComp from './SingleCardComp.vue'

export default {
    name: "CardsComp",
    components: {
        SingleCardComp
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="d-flex flex-wrap justify-content-between bg-white">
        <SingleCardComp v-for="(elem, index) in store.arrayCards" :key="index" :dettagliCard="elem" />
    </div>
</template>

<style lang="scss"></style>