<template>
    <AppHeader />
</template>

<script>
  import AppHeader from './components/AppHeader.vue';
  export default {
    nome: "App",
    components: {
      AppHeader,
    },
  }
</script>

<style lang="scss">
@import "./style/global.scss";
</style>