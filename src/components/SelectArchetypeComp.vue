<script>
import axios from 'axios';

export default {
    name: "SelectArchetypeComp",
    data() {
        return {
            archetypes: []
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then(res => {
                for (let i = 0; i < res.data.length; i++) {
                    this.archetypes.push(res.data[i]);
                }
            })
    }
}
</script>

<template>
    <select class="form-select" aria-label="Default select example">
        <option selected>Select Archetype</option>
        <option v-for="archetype in archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>

    </select>
</template>

<style lang="scss">
select {
    width: 200px !important;
    margin: 30px auto !important;
}
</style>