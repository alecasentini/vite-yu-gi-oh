<script>
import axios from 'axios';
import { store } from '../store';

export default {
    name: "SelectArchetypeComp",
    data() {
        return {
            store,
            archetypes: [],
            // selectedArchetype: "",


        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then(res => {
                for (let i = 0; i < res.data.length; i++) {
                    this.archetypes.push(res.data[i]);
                }
            })
    },
    methods: {
        selectChange() {

            axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${this.store.selectedArchetype}`)
                .then(res => {

                    const datiApi = res.data.data

                    this.store.arrayCards = datiApi
                })
        }
    }

}
</script>

<template>
    <select class="form-select" aria-label="Default select example" v-model="this.store.selectedArchetype"
        @change="selectChange">
        <option selected value="">Select Archetype</option>
        <option v-for="archetype in archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>

    </select>
</template>

<style lang="scss">
select {
    width: 200px !important;
    margin: 30px auto !important;
}
</style>