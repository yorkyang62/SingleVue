<template>
  <p>{{msg}}</p>
</template>
<script>
    export default {
      data () {
        return {
        }
      },
      props:['msg']  // 添加 props 接收父元传递过来的数据。
    }
</script>