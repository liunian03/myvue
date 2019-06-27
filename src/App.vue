<template>
    <div id="app">
        <!--<img src="./assets/logo.png">-->
        <v-header></v-header>
        <v-blog title="I am title"></v-blog>
        <v-blog v-bind:title="post.title"></v-blog>
        <v-demo></v-demo>
    </div>
</template>

<script type="text/ecmascript-6">

    import header from './components/header';
    import blog from './components/blog-test';
    import exDemo from "./components/exDemo";

    export default {
        data() {
            return {
                count:0,
                post:{
                    title:'我是标题'
                }
            }
        },
        // created(){//钩子
        //   this.$http.get('/api/sellers').then((response)=>{
        //     // response = response.json();
        //     // if(response.errno===ERR_OK){
        //       this.sellers = response.data;
        //       console.log(this.sellers);
        //     // }
        //   },(err)=>{console.log(err)});
        // },
        name: 'App',
        components: {
            'v-header':header,
            'v-blog':blog,
            'v-demo':exDemo
        }
        
    }
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import "./common/stylus/mixin.styl"
    #app
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: left;
        color: #2c3e50;
        /*padding: 0.15rem;*/
        font-size:0.28rem;
    
</style>
