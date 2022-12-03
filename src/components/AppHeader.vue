<template>
    <input type="text" placeholder="Search a movie" v-model="store.SearchText">
    <button>Search</button>
</template>

<script>
    import {store} from "../store";
    export default {
        name: "AppHeader",
        data() {
            return {
                store,
            };
        },
    }
</script>

<style lang="scss" scoped>

</style>