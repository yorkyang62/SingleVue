<template>
    <div>
        <h1>哈哈哈：{{name}}</h1>
    </div>
</template>
<script>
    //es6
    export default {
         //data:function(){}，下面是es6写法
         data () {
            return {
                name:"杨胜"
            }
        }
    }
</script>
<style lang="sass">
    /*一定要加lang不然无法编译*/
    /*测试一下对sass的编译*/
    $qwe:#098;
    body{
        background-color: $qwe;
        h1{
            background-color: #eee;
            color: red;
            transform: translate(10%, 10%);/*测试自动添加前缀*/
        }
        h1:hover{
            height:100px;
        }
        h2{
            background-color: #999;
        }
    }
</style>