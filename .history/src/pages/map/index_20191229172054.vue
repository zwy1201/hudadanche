<template>
  <div>
         
  
</i-card>

    </div>
</template>

<script>
export default {
  data () {
    return {
     list:[]
      
    }
  },
   onLoad(option){
  this.list = require('@/data/' + option.type + '.json')
  console.log(this.list)
   },
  methods: {
  
  },
  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
div >>> .split{
  margin-bottom:10pt;
}
</style>