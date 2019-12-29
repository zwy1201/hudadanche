<template>
  <div style="width:100%;height:100%;">
         <map id="map" scale="14"  :markers="markers" show-location style="width: 100%; height: 100%;"></map>
  


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