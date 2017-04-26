<template>
  <p v-for="list in mesFather">{{list}}</p>
  <input type="text" v-model="msg" @keyup="onInput">
</template>
<script>
    export default {
      data () {
        return {
          msg: 'Welcome to Your Vue.js App'
        }
      },
      methods: {
          onInput: function () {
            if (this.msg.trim()) {
              this.$emit('message', this.msg);
            }
          }
        },
      props:['mesFather']  // 添加 props 接收父元传递过来的数据。
    }
</script>