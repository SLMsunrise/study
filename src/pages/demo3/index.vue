<template>
  <div>
    <div>计算属性</div>
    <div>-------------------------</div>
    <div>{{sd}}</div>
  </div>
</template>

<script>
  export default {
    name: '',
    data () {
      return {
        msg:'slm'
      }
    },
    computed: { //计算属性
      sd() {    //函数名称
        // return this.msg.split('').reverse().join('');//反转函数
        return this.msg+"wcm"//通过return返回需要做的计算或者表达式
      }
    },
    methods:{

    }
  }
</script>

<style scoped>

</style>
