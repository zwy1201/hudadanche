<template>
  <div>
          const setting = {
          skew: 0,
          rotate: 0,
          showLocation: false,
          showScale: false,
          subKey: '',
          layerStyle: -1,
          enableZoom: true,
          enableScroll: true,
          enableRotate: false,
          showCompass: false,
          enable3D: false,
          enableOverlooking: false,
          enableSatellite: false,
          enableTraffic: false,
        }

        this.setData({
          // 仅设置的属性会生效，其它的不受影响
          setting: {
            enable3D: true,
            enableTraffic: true
          }
        })


  
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