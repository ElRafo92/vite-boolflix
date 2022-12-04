<template>
    <form @submit.prevent="$emit('performSearch')">
        <input type="text" placeholder="Search a movie" v-model="store.SearchText" required>
        <button type="submit" >Search</button>
    </form>
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