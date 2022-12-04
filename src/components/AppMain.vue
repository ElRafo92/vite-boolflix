<template>
    <div>
        <AppCard v-for="movie in store.movies" :info="movie" />
    </div>
</template>

<script>
    import { store } from "../store";
    import AppCard from './AppCard.vue';
    export default {
        name: "AppMain",
        components: {
            AppCard,
        },
        data() {
            return {
                store,
            };
        },
    }
</script>

<style lang="scss" scoped>

</style>