<template>
  <div class="qui-nav nav-type-1">
    <a v-for="(item, index) in items" :class="[commonClass,item.active ? activeClass : '']" v-on:click="navClickEvent(items,index)">
      <span class="nav-txt">{{item.text}}</span>
    </a>

  </div>
</template>

<script>
  export default {
    data:function(){
      return {
        items:[
          {
            text: '首页',
            active : true
          },
          {
            text: '列表',
            active : false
          },
          {
            text: '关于',
            active : false
          },
          {
            text: '招聘',
            active : false
          }
        ],
        commonClass:'nav-item',
        activeClass:'active',
      }
    },
    methods:{
      navClickEvent:function (items,index) {
        items.forEach(function (el) {
          el.active=false;
        })
        items[index].active = true;
        /*开放用户自定义的接口*/
        this.$emit('navClickEvent',items,index);
      }
    }
  }

</script>

<style scoped>
  .active{
    border-bottom: 2px solid red;
  }
</style>
