<template>
    <div>
        <h3>{{info.title}}</h3>
        <h4>{{info.original_title}}</h4>
        <div>{{info.original_language}}</div>
        <div>{{info.vote_average}}</div>
    </div>
</template>

<script>
    export default {
        name: "AppCard",
        props: {
            info: Object,
        },
    };
</script>

<style lang="scss" scoped>
    div {
        margin: 30px 0px;
    }
</style>