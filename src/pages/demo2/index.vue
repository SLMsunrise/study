<template>
<div>
  <div>模板语法</div>
  <div>---------------------------</div>
  <div>data:{{msg}}</div>
  <div>---------------------------</div>
  <div>{{num+1}}</div>
  <div>---------------------------</div>
  <div>
    指令for
    <li v-for="item in items" :key="item.name">
      {{item.name}}
    </li>
  </div>
  <div>---------------------------</div>
  <div v-bind:class="red" v-on:click="change">
    {{red}}
  </div>
  <div>---------------------------</div>
  <div>
    {{messages|capitalize}}
  </div>


</div>
</template>

<script>
  export default {
    name: '',
    data(){
      return{
        msg:'数据绑定',
        num:1,
        items:[
          {name: "slm"},
          {name: "wcm"},
          {name: "果果"},
          {name: "妹妹"}
          ],
        red:'red',
        message:"史黎明是大笨蛋"
      }
    },
    methods:{   //事件方法
      change(){
        this.red="blue"
      }
    },
    filters:{   //过滤器
        capitalize(){
          return '123'
        }
    }
  }
</script>

<style scoped>
.red{
  color: red;
}
  .blue{
    color: blue;
  }
</style>
