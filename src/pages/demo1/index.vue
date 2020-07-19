<template>
  <div>
    <div>选项数据</div>
    <div>-----------------</div>
    <div>{{msg}}</div>
    <div>-----------------</div>
    <div>computed:{{aDouble}}</div>
    <div>-----------------</div>
    <div v-on:click="eventClick">Event</div>
  </div>
</template>

<script>
  export default {
    // name: '',
    data(){
      return{
        msg:"史黎明", //数据绑定
        num:2
      }
    },
    computed:{      //对象中包含的函数
      aDouble(){
        return this.num * 2;
      }
    },
    methods:{       //事件函数
      eventClick:function () {
        alert("我是一个方法")
      }
    }
  }
</script>

<style scoped>

</style>
