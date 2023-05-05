<script>
import { store } from '../store'
export default {
    name: "CountCardComp",
    data() {
        return {
            store
        }
    }

}
</script>

<template>
    <div id="count" class="d-flex">
        <h4 class="text-white d-flex align-items-center ps-5">Found {{ store.arrayCards.length }} card</h4>
    </div>
</template>

<style lang="scss">
#count {
    background-color: #212529;
    height: 70px;
}
</style>