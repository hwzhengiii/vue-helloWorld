<template>
  <div>
    {{msg}}
  </div>
</template>

<script>
import api from "../api";
export default {
  name: "test",
  data(){
    return{
      msg:''
    }
  },
  mounted () {
    this.getMsg()
  },
  methods:{
    getMsg () {
      let funcName = 'getMsg'
      api[funcName]().then(res => {
        this.msg=res
      })
      },
    }
}
</script>

<style scoped>

</style>
