<template>
    <div>
      <div>class和style绑定</div>
      <div v-bind:class="{'active':isActive,'text-danger':hasError}">我会变class1</div>
      <div v-bind:class="classobject">我会变class2</div>
      <div v-bind:class="[gg,mm]">我会变class3</div>
      <div>------------------------------------</div>
      <div>
        <h3 id="btn" v-on:click="btn" v-bind:style="{color:activeColor.blue}">我会自动变色</h3>
      </div>

      <div>条件渲染</div>
      <div>------------------------------------</div>
      <div v-if="ok">
        ok?ay?
      </div>
      <div v-else-if="or">
        或者？or?
      </div>
      <div v-else>
        只能这样了
      </div>
      <div v-show="showD">
        show??
      </div>

      <div>列表循环</div>
      <div>------------------------------------</div>
      <div>
        <!--数组时，第二个参数是数组下标-->
        <li v-for="(arr,index) in arrlist" :key="arr.name">
          {{index}}-{{arr.name}}
        </li>

        <!--对象时，第二个参数是key值-->
        <li v-for="(value,name) in objListArr">
          {{name}}-{{value}}
        </li>
      </div>

      <div>多选框</div>
      <div>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
      <label for="jack">Jack</label>
      <span>Checked names: {{ checkedNames }}</span>
      </div>

      <div>单选框</div>
      <div>
        <input type="radio" id="one" value="One" v-model="picked">
        <label for="one">One</label>
        <input type="radio" id="two" value="two" v-model="picked">
        <label for="one">Two</label>
        <span>Picked: {{ picked }}</span>
      </div>

      <div>
        过滤输入的空白字符：<input v-model.trim="msg">
        <div>{{msg}}</div>
      </div>



    </div>
</template>

<script>
  export default {
    name: '',
    data(){
      return{
        isActive:true,
        hasError:false,
        classobject:{
          'slm':true,
          'wcm':false
        },
        gg:"guo",
        mm:"mei",
        activeColor:{
          red:"red",
          blue:"blue"
        },
        ok:false,    //条件渲染
        or:false,     //
        showD:true,
        arrlist:[     //数组模式
          {name:"床前明月光"},
          {name:"疑是地上霜"},
          {name:"举头望明月"},
          {name:"低头思故乡"}
        ],
        objListArr:{  //对象模式
            num:"风雨飘零夜",
            slm:"何处是安生"
        },
        checkedNames: [],    //input选择框
        picked:'',
        msg:''
      }
    },
    methods:{
      btn(){
        this.activeColor.blue="pink"
      }
    },
  }

</script>

<style scoped>
.red{
  color: red;
}
  .blue{
    color: blue;
  }
  .pink{
    color: pink;
  }
</style>
