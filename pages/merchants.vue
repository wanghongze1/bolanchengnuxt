<template>
  <div class="container">
    <Header/>
    <img class="mer-banner" src="~/assets/img/banner.png" alt="">
    <img src="~/assets/img/typemer.png" alt="" class="mer-type-title">

    <div class="mer-box-one-m">
      <div class="mer-box-one-m-i" v-for="item in typeList" key="index">
        <img :src="item.img" alt="" class="mer-box-one-m-img">
        <p class="mer-box-one-m-text">{{item.name}}</p>
      </div>
    </div>

    <img src="~/assets/img/mertjjp.png" alt="" class="mer-tjjp-title">

    <div class="mer-box-two-m">
      <div class="mer-box-two-m-i" v-for="i in 9" >
        <img src="~/assets/img/mjpt.png" alt="" class="mer-box-two-m-img">
        <h3 class="mer-box-two-m-pingpai">椅子</h3>
        <p class="mer-box-two-m-p">姓名：张三</p>
        <p class="mer-box-two-m-p">电话：18888888888</p>
        <div class="mer-box-two-weizi">
          <img src="~/assets/img/weizhiicon.png" alt="" class="mer-box-two-weizi-img">
          <div class="mer-box-two-weizi-text">A1-939</div>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
import Header from '@/components/Header';
export default {
  data() {
    return {
      typeList:[{
        name:'椅子',
        img:require('~/assets/img/myz.png')
      },{
        name:'电视柜',
        img:require('~/assets/img/mdsg.png')
      },{
        name:'餐桌',
        img:require('~/assets/img/mcz.png')
      },{
        name:'衣帽架',
        img:require('~/assets/img/mymj.png')
      },{
        name:'茶几',
        img:require('~/assets/img/mcj.png')
      },{
        name:'酒店家具',
        img:require('~/assets/img/mjdjj.png')
      },{
        name:'户外家具',
        img:require('~/assets/img/mhwjj.png')
      },{
        name:'办公家具',
        img:require('~/assets/img/mbgjj.png')
      },{
        name:'沙发',
        img:require('~/assets/img/msf.png')
      },{
        name:'校用家具',
        img:require('~/assets/img/mxyjj.png')
      },{
        name:'学习桌',
        img:require('~/assets/img/mxxz.png')
      },{
        name:'其他',
        img:require('~/assets/img/mqt.png')
      }],
    };
  },
}
</script>

<style scoped>
.mer-banner{
  width: 100%;
  min-width: 1400px;
}
.mer-type-title{
  width: 348px;
  height: 60px;
  display: block;
  margin: 94px auto 51px;
}
.mer-box-one-m{
  width: 100%;
  max-width: 1400px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.mer-box-one-m-i{
  width: 218px;
  height: 110px;
  position: relative;
  margin: 0 0 20px 0;
  cursor: pointer;
}
.mer-box-one-m-img{
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
.mer-box-one-m-text{
  font-family: PingFangSC-Regular;
  font-size: 20px;
  color: #FFFFFF;
  text-align: center;
  line-height: 110px;
}
.mer-tjjp-title{
  width: 814px;
  height: 60px;
  display: block;
  margin: 74px auto 51px;
}
.mer-box-two-m{
  width: 100%;
  max-width: 1400px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 0 0 40px 0;
}
.mer-box-two-m-i{
  width: 434px;
  padding: 0 0 28px 0;
  position: relative;
  box-shadow: 0 0 8px 0 rgba(0,0,0,0.24);
  margin: 0 0 49px 0;
}
.mer-box-two-m-img{
  width: 434px;
  height: 294px;
}
.mer-box-two-m-pingpai{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #000000;
  margin: 26px 0 12px 30px;
}
.mer-box-two-m-p{
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #333333;
  margin: 0 0 0 30px;
}
.mer-box-two-weizi{
  position: absolute;
  bottom: 48px;
  right: 30px;
  text-align: center;
}
.mer-box-two-weizi-img{
  width: 26px;
  height: 30px;
}
.mer-box-two-weizi-text{
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #B71C22;
}
</style>
