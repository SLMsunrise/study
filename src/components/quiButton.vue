<template>
  <button class="qui-btn" v-on:click="btnClickEvent">
    <slot name="icon"></slot><!--重点在这里-->
    <span>{{msg}}</span>
  </button>
</template>

<script>
  export default {
    props: {    //props是专门用来暴露组件的属性接口的
      msg: {
        default: '下载'
      }
    },
    methods:{
      btnClickEvent: function(){
        alert("先弹出默认的文案");
        this.$emit('btnClickEvent');//关键代码父组件触发自定义事件
        //  $emit，也叫触发机制，父组件监听，子组件触发
      },
    }
  }
</script>

<style scoped>

</style>
