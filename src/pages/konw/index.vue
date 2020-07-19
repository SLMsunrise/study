<template>
  <div>
    <div>
      Vue使用:
      插值、表达式、指令、动态属性。<br>
      computed有换缓存，data不变数据不变。<br>
      watch中deep:true是深度监听，拿引用类型。<br>

      <li>
        1, v-show和v-if的区别？使用场景？
        答：v-if渲染的东西，只渲染结果为true的内容，v-show都渲染出来，将true结果显示，false结果隐藏。<br>频繁切换时使用v-show.如tab切换。
      </li>
      <li>
        2，key的重要性。（v-if和v-for不能一起使用）
      </li>
      <li>
        3，事件的参数"&event"是挂载当前元素下。
        <button @click.ctrl.exact="onCtrlClick">A</button>
      </li>
      <li>
        4，props组件的传递、$emit事件的触发、组件间通讯-自定义事件、组件生命周期
        生命周期：挂载-更新-删除<br>
        created:指vue实例化完成，页面还没有开始渲染；<br>
        mounted:指页面渲染完成后，执行的操作。<br>

        父子组件的生命周期：先将父组件初始化完毕，再初始化子组件。在渲染时，先渲染子组件，再渲染父组件。<br>
      </li>
      <li>
        5，高级特性：
        自定义v-model、$nextTick、slot、动态异步组件、keep-alive、mixin。
        vue是异步渲染。<br>
        （1）.ref="name"可以使用this.$refs.name获取当前节点的dom元素；<br>
        （2）.this.$nextTick(()=>{body})//dom渲染完之后再回调,页面渲染时会将data的修改做整合，多次修改且只会渲染一次。<br>
        （3）.slot基本使用：父组件往子组件插入内容。

      </li>
      <li>
        6，动态组件：<br>
        :is="component-name"的用法<br>
      </li>
      <li>
        7，异步组件：加载大组件<br>
        import()函数
        formdemo:()=>important('组件')
      </li>
      <li>
        8，keep-alive缓存组件:频繁切换，不需要重复渲染<br>
      </li>
      <li>
        9，mixin多个组件有相同的逻辑，抽离出来。<br>
        mixins:[myMixin,myMixin2]//可以添加多个。
        存在的问题：变量来源不明确、多mixin可能会造成命名冲突、mixin和组件可能出现多对多的关系，复杂度较高。

      </li>
      <li>
        10，vuex:状态管理<br>

      </li>
      <li>
        11，vue原理：（1）：组件化、（2）：响应式、（3）：vdom和diff、（4）：模板编译、（5）：渲染过程、（6）：前端路由<br>
        组件化基础：MVVM模型、根据数据重新渲染视图。Model-View-ViewModel
      </li>
      <li>
        12，data的数据变化：核心API-Object.defineProperty<br>
        vue如何监听数组变化、DOM-diff、vdom虚拟Dom、模板编译、vue组件是如何渲染和更新的、
      </li>
      <li>
        （1）、 v-for中使用key?答：diff算法中通过tag和key来判断，是否是sameNode，减少渲染次数提升渲染性能。<br>
        （2）、 Vue生命周期？答：<br>
        （3）、 Vue组件如何通讯？答：父子组件：通讯props和this.$emit。自定义组件：event.$no、event.$off、event.$emit 状态管理（vuex）<br>
        （4）、 双向数据绑定v-model的实现原理： input输入的value值、会绑定$event.target.value,然后触发re-render<br>
        （5）、 对MVVM的理解： <br>
        （6）、 computed的特点：有缓存、data不变就不会重新计算，提高性能。<br>
        （7）、 组件data为什么是一个函数？定义的组件是一个类，使用这个类的时候相当于是类的一个实例化。<br>
        （8）、 ajax的请求应该放在哪个生命周期？mounted里面，即页面渲染完成后。因为js是单线程的，Ajax异步获取。 <br>
        （9）、 如何实现自己的v-model? <br>
        （10）、如何处理相同逻辑的组件？如何抽离？mixin、  <br>
        （11）、何时使用异步组件？加载大组件、路由异步加载。  <br>
        （12）、何时使用keep-alive? 缓存组件、不需要重新渲染。多个tab切换中。 <br>
        （13）、vuex中的action和mutation的区别？action中处理异步、mutation不可以。action可以整合多个mutation。  <br>
        （14）、vue-router常用的路由模式？hash默认、H5 history  <br>
        （15）、如何配置vue-router异步加载？  <br>
        （16）、data的数据变化：核心API-Object.defineProperty（不能监听数组变化） ，proxy可以支持。 <br>
        （17）、  <br>
        （18）、  <br>
        （19）、  <br>
        （20）、  <br>

      </li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>

    </div>
  </div>
</template>

<script>
  export default {
    name: '',
    data(){

      return{

      }
    },
    methods:{
      onCtrlClick:function () {
        alert('A')
      }
    }
  }
</script>

<style scoped>

</style>
