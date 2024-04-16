<template>
  <div class="hello">
    <el-button type="primary" @click="handle">点击打开输入框并获取时间</el-button>
    <el-input v-show="isShow" v-model="input" style="width: 240px" placeholder="请输入关键词" />
    <el-tag v-show="isShow" type="primary">{{ time }}</el-tag>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      input:'',
      isShow:false,
      time:''
    }
  },
  methods:{
    handle(){
      this.isShow = !this.isShow
      this.time = new Date()
    }
  },
  created(){
    this.time = new Date()
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
