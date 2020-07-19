<template>
    <div>
      <div>

          <div v-for="item in items" :key="item.name">
            作者：{{item.name}}--标题：{{item.title}}
          </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: '',
    data(){
      return{
        items:[]
      }
    },
    mounted(){  // 生命周期函数
      this.$http.get('/api/public/wchat.php').then(response=>{
        console.log(response.body);
        this.items=response.body;// 通过this指向date名
      },response=>{

      })

    }
  }
</script>

<style scoped>

</style>
