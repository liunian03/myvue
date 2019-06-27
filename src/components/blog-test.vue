<template>
    <h1>{{title}}</h1>
</template>

<script>
    export default {
        name: "blog-test",
        props:['title']
    }
</script>

<style lang="stylus" rel="stylesheet/stylus">
    h1
        font-size:30px;
</style>