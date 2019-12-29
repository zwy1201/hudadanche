<template>
  <div>
    <swiper
      :indicator-dots="indicatorDots"
        :autoplay="autoplay" 
        :interval="interval" 
        :duration="duration"
        >
<block v-for="img in imgUrls" :key="img">
          <swiper-item>
            <image :src="img" style="width：100%" />
          </swiper-item>
        </block>
      </swiper>

      	   <i-grid i-class="no-border">
    <i-grid-item @click="goType(grid)" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
    </i-grid-item>
</i-grid>


 <i-panel :title="title_name">
    <view style="padding: 15px;">
       <i-card  v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.iamge">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">{{item.address}}</view>
</i-card>
      

</view>
</i-panel>
    
  </div>
</template>

<script>


export default {
  data () {
    return {
     title_name:"推荐",
     grids:[
       
            {title:"小黄车",image:"/static/images/1.png"},
            {title:"小蓝车",image:"/static/images/2.png"},
            {title:"摩拜",image:"/static/images/3.png"},
            {title:"租八戒电动车",image:"/static/images/4.png"}
       
     ],
     top:[
       {name:"编号1",address:"",image:"8.jpg",remark:"介绍1" },
       {name:"编号2",address:"地址2",image:"9.jpg",remark:"介绍2" },
       {name:"编号3",address:"地址3",image:"10.jpg",remark:"介绍3" },
       {name:"编号4",address:"地址4",image:"12.jpg",remark:"介绍4" }
     ],
      imgUrls: [
      "/static/images/5.jpg",
      "/static/images/6.jpg",
      "/static/images/7.jpg"
    ],
    indicatorDots: false,
    autoplay: false,
    interval: 5000,
    duration: 1000
    }
    
  },

  

  methods: {
       goType(type){
        console.log(type)
        let url = '../list/main?type=' + type.title
        mpvue.navigateTo({ url })
    }

  },

  created () {
 
  }
}
</script>

<style scoped>
 div >>> .no-border{
  border-width:0pt;
}
div >>> .split{
  margin-bottom:10pt;
}
</style>
