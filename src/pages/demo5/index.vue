<template>
  <div>
    <div>自定义组件</div>
    <div>---------------------------------</div>
    <slm></slm>
    <slm></slm>
    <slm></slm>
    <slm></slm>

    <button v-on:click="show=!show">
      Toggle
    </button>
    <transition name="fade">
      <p v-if="show">hello</p>
    </transition>

    <div>状态管理:它采用集中式存储管理应用的所有组件的状态，并以相应的规则保证状态以一种可预测的方式发生变化。</div>
    <div>{{msg}}</div>
    <button @click="change">
      change
    </button>

    <div>插槽：常用于组件调用</div>
    <slm></slm>

  </div>
</template>
<script>
  import slm from '../../components/zujian.vue'   //引入组件
  export default {
    name: '',
    data(){
      return{
        show:true,
        msg:"123"
      }
    },
    methods:{
      change () {
        //vuex取数据
        // this.msg=this.$store.state.count;
        //vuex修改数据
        this.$store.dispatch('inc',10000);
        this.msg=this.$store.state.num;
      }
    },
    components:{                                  //注册组件
      'slm':slm,
    }
  }
</script>

<style scoped>
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to{
    opacity: 0;
  }
</style>
