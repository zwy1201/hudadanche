<template>
  <div>
         <map id="map" longitude="113.324520" latitude="23.099994" scale="14" controls="{{controls}}" bindcontroltap="controltap" markers="{{markers}}" bindmarkertap="markertap" polyline="{{polyline}}" bindregionchange="regionchange" show-location style="width: 100%; height: 300px;"></map>
  


    </div>
</template>

<script>
export default {
  data () {
    return {
     list:[]
      
    }
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