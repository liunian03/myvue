<template>
    <div class="container">
<!--        图片-->
        <div class="increase" v-bind:class="{burst:ended}"></div>
<!--        进度条情况-->
        <div class="progressbar">
            <div v-bind:style="{width:progess + '%'}"></div>
        </div>
<!--        按钮-->
        <div class="controlls">
            <button @click="touch" v-show="!ended">使劲敲</button>
            <button @click="restart">重新加载</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "exDemo",
        data(){
            return{
                progess:100,
                ended:false
            }
        },
        methods:{
            touch:function(){
                this.progess -= 10;
                if(this.progess <= 0){
                    this.ended = true;
                }
            },
            restart:function(){
                this.progess = 100;
                this.ended = false;
            }
        }
    }
</script>

<style scoped>
    .container{
        width:500px;
        margin:0 auto;
    }
    .increase{
        width:200px;
        height:200px;
        background-image:url("../assets/bag.png");
        background-size:40% 90%;
        background-repeat:no-repeat;
        background-position: center;
    }
    .increase.burst{
        background-image:url("../assets/bag-burst.png");
    }
    .progressbar{
        width:200px;
        border:2px solid #000;
        margin-bottom:20px;
    }
    .progressbar div{
        height:20px;
        background: #9c051f;
    }
    .controlls button{
        margin-left:20px;
    }
</style>