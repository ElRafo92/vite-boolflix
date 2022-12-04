<template>
    <AppHeader @performSearch="getData" />
    <AppMain />
</template>

<script>
  import axios from "axios";
  import AppHeader from './components/AppHeader.vue';
  import AppMain from "./components/AppMain.vue";
  import { store } from "./store";

  export default {
    nome: "App",
    components: {
      AppHeader,
      AppMain,
    },
    data() {
      return {
        store
      }; 
    },
    methods: {
      getData() {
        axios.get("https://api.themoviedb.org/3/search/movie", {
          params: {
            query: this.store.SearchText,
            api_key:'33a809853c696dc844a8d636f167b7a1',
            lenguage: 'it-IT',
          },
        })
        .then((resp) => {
          this.store.movies = resp.data.results;
        });
      },
    },
  }
</script>

<style lang="scss">
@import "./style/global.scss";
</style>