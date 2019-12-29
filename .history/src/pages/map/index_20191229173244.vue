<template>
  <div style="width:100%;height:100%">
         <map id="map" longitude="113.324520" latitude="23.099994" scale="14" controls="{{controls}}" bindcontroltap="controltap" markers="{{markers}}" bindmarkertap="markertap" polyline="{{polyline}}" bindregionchange="regionchange" show-location style="width: 100%; height: 300px;"></map>
  


    </div>
</template>

<script>
export default {
  data () {
    return {
     markers: [{
      iconPath: "/resources/others.png",
      id: 0,
      latitude: 23.099994,
      longitude: 113.324520,
      width: 50,
      height: 50
    }],
      
    }
  },
 
  methods: {
  
  },
  created () {
    // let app = getApp()
  }
}
</script>

<style>
div >>> .split{
  margin-bottom:10pt;
}
</style>