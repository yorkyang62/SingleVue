<template>
    <div>
        <h1>姓名：{{name}}</h1>
        <h2>{{age}}</h2>
        <hello :mes-father="sendValue" v-on:message="recieveMessage"></hello>
        <test :msg="msg"></test>
    </div>
</template>
<script>
    //es6
    import hello from './hello';
    import test from './test';
    export default {
         //data:function(){}，下面是es6写法
         data () {
            return {
                show: true,
                name:"guowenfh",
                age:"2q1",
                sendValue:[1,2,3]
            }
        },
        components: {
            'hello': hello,
            'test':test
        },
        methods: {
          recieveMessage: function (text) {
            console.log('监听到子组件变化'+text);
          }
        },
        props:['msg']
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