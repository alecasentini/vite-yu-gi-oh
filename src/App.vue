<script>
import axios from 'axios';
import { store } from './store'
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

export default {
    name: "App",
    components: {
        HeaderComp,
        MainComp
    },
    data() {
        return {
            store
        }
    },
    methods: {
        selectChange() {
            axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${store.selectedArchetype}`)
                .then(res => {

                    const datiApi = res.data.data

                    this.store.arrayCards = datiApi
                })
        }
    }
}
</script>

<template>
    <HeaderComp />
    <MainComp />
</template>

<style lang="scss">
@use "./style/main.scss" as *;
</style>
