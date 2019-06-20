<template>
    <div class="test">
        {{'2018'| filterA | filterB}}
    </div>
</template>

<script>
    export default {
        name: "headerNav",
        methods:{
        
        },
        filters:{
            filterA:function(value){
                return value + "年"
            },
            filterB:function(value){
                return value + 'hello word'
            }
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>