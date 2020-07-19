<template>
  <div id="pageQuiButton">
    <!--使用-->
    <qui-btn v-on:btnClickEvent="doSth1" msg="确定" >
      <img slot="icon" class="ico" src="../images/xiaz.png" width="16"/>
    </qui-btn>
    <qui-btn v-on:btnClickEvent="doSth2" msg="取消" >

    </qui-btn>
  </div>
</template>
<script>
  import quiBtn from '../components/quiButton.vue' /*引用*/
  export default {
    name: 'pageQuiButton',
    components: {
      'qui-btn': quiBtn /*注册自定义标签*/
    },
    methods:{
      doSth1: function(){
        alert('111');
      },
      doSth2: function(){
        alert('222');
      }
    }
  }
</script>
<style scoped>


</style>
