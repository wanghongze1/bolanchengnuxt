<template>
  <div class="container" >
    <!-- <div :style="{width: screeWidth + 'px'}"> -->
      <img src="~/assets/img/indexbg.png" alt="" class="indexbg" >
      <div style="height:71px;"></div>
      <div class="box">
        <div class="middle-box-one">
          <div class="middle-one-box-left">
            <img src="~/assets/img/logo.png" alt="" width="100%" >
          </div>
          <div class="middle-one-box-right">
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/`}">
              <span>首页</span>
              <img src="~/assets/img/index1.png" alt="">
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/`}">
              <span>展会专区</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/onlineMerchant`}">
              <span>在线招商</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/merchants`}">
              <span>商家展示</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/news`}">
              <span>新闻中心</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/talent`}">
              <span>人才招聘</span>
            </nuxt-link>
            <nuxt-link style="padding:0 0 0 20px" class="middle-one-box-right-item" :to="{path: `/about`}">
              <span>关于我们</span>
            </nuxt-link>
          </div>
        </div>

        <div class="middle-box-two">
          <img src="https://hongshuye01.oss-cn-beijing.aliyuncs.com/mall/banner/image/20200906/8ae3e65f5a194c6e934faff5be3937ae.png" alt="">
          <div class="middle-box-two-tian">{{days}}</div>
          <div class="middle-box-two-shi">{{hours}}</div>
          <div class="middle-box-two-fen">{{minutes}}</div>
          <div class="middle-box-two-miao">{{seconds}}</div>
          <img src="~/assets/img/index3.png" alt="" class="index3-img">
        </div>
        <img src="~/assets/img/index4.png" alt="" class="index4-img">

        <div class="middle-box-three">
          <img src="~/assets/img/index5.png" alt="" class="index5-img">
          <div class="middle-box-three-m">
            <img src="~/assets/img/index6.png" alt="" class="index6-img">
            <div class="address">公司地址：河北廊坊胜芳国际家具博览中心</div>
          </div>
        </div>

        <div class="middle-box-four">
          <img src="~/assets/img/index7.png" alt="" class="index7-img">
        </div>

        <div class="middle-box-five">
          <div class="middle-box-five-m">
            <div class="middle-box-five-m-l">
              <!-- <img src="@/assets/img/index3.png" alt="" width="100%"> -->
            </div>
            <div class="middle-box-five-m-r">
              <h4 class="middle-box-five-m-r-title">胡桃木家具设计风格</h4>
              <p class="middle-box-five-m-r-p">传统与现代的碰撞，是现代生活方式与传统文化其优秀部分的完美糅合，撇去了古典元素的老成，却多了一份自然、...</p>

              <div class="middle-box-five-m-r-t-list">
                <div class="middle-box-five-m-r-t-list-item" v-for="(i, index) in 5" :key="index">
                  <div class="middle-box-five-m-r-t-list-item-l">
                    <img src="~/assets/img/index8.png" alt="">
                    <h4>胡桃木家具设计风格</h4>
                  </div>
                  <div class="middle-box-five-m-r-t-list-item-r">
                    06-23
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="middle-box-six">
          <img src="@/assets/img/index9.png" alt="" class="index9-img">
          <div class="middle-box-six-m">
            <img src="@/assets/img/index10.png" alt="" class="index10-img">
            <div class="middle-box-six-btn1" :style="{color:(tabnum == 1 ? '#FF6E0A' : '#FFF'),border:(tabnum == 1 ? '1px solid #FF6E0A' : '1px solid #FFFFFF')}" @click="tabBtn(1)">实时地图</div>
            <div class="middle-box-six-btn2" :style="{color:(tabnum == 2 ? '#FF6E0A' : '#FFF'),border:(tabnum == 2 ? '1px solid #FF6E0A' : '1px solid #FFFFFF')}" @click="tabBtn(2)">交通图</div>
            <div v-if="tabnum == 1">
              <div class="middle-box-six-adress">
                <h3>场地：</h3>
                <p>胜芳国际家具博览中心</p>
              </div>
              <div class="middle-box-six-adress middle-box-six-adress1">
                <h3>场地：</h3>
                <p>成都新国际会展中心</p>
              </div>
              <div class="middle-box-six-map">
                地图展示
              </div>
            </div>
            <img v-else src="@/assets/img/jtnrzn.png" alt="" class="jtnrzn-img">
            
          </div>
        </div>

        <div class="middle-box-seven">
          <img src="@/assets/img/index12.png" alt="" class="index12-img">
          <div class="common-middel middle-box-seven-m">
            <img src="@/assets/img/index13.png" alt="" class="index13-img">
            <SwiperDetail></SwiperDetail>
          </div>
        </div>

        <div class="middle-box-eight">
          <img src="@/assets/img/index14.png" alt="" class="index14-img">
          <div class="common-middel middle-box-eight-m">
            <img src="@/assets/img/index15.png" alt="" class="index15-img">
            <SwiperCategory></SwiperCategory>
          </div>
        </div>

        <div class="middle-box-nine">
          <img src="@/assets/img/index17.png" alt="" class="index17-img">
          <div class="common-middel middle-box-nine-m">
            <img src="@/assets/img/index18.png" alt="" class="index18-img">
            <div class="middle-box-nine-m-ping">
              <img src="@/assets/img/ping1.png" alt="">
              <img src="@/assets/img/ping2.png" alt="">
              <img src="@/assets/img/ping3.png" alt="">
              <img src="@/assets/img/ping4.png" alt="">
              <img src="@/assets/img/ping5.png" alt="">
              <img src="@/assets/img/ping6.png" alt="">
              <img src="@/assets/img/ping7.png" alt="">
              <img src="@/assets/img/ping8.png" alt="">
              <img src="@/assets/img/ping9.png" alt="">
              <img src="@/assets/img/ping10.png" alt="">
            </div>
          </div>
        </div>
        
        <!-- 左边小人 -->
        <nuxt-link :to="{path: `/onlineMerchant`}">
          <img src="@/assets/img/ruzu.png" alt="" class="ruzu-img">
        </nuxt-link>
        <!-- 右边 @mouseout="lianxiMouseover(2)"  v-if="rightlianxibig == 1"  v-else -->
        <img src="@/assets/img/lianxi.png" alt="" class="lianxi-img">
        <div class="lianxibig-box" >
          <img src="@/assets/img/lianxibig.png"  alt="" class="lianxibig-img">
          <div class="lianxibig-box-one"></div>
           <!-- <div class="lianxibig-box-two"></div> -->
           <img src="@/assets/img/erweima.png" alt="" class="erweima1">
         <!-- <img v-if="erweima2" src="@/assets/img/erweima.png" alt="" class="erweima2"> -->
        </div>
        
      </div>
    <!-- </div> -->
  </div>
</template>
 
<script>
import moment from 'moment'
import SwiperDetail from '@/components/SwiperDetail';
import SwiperCategory from '@/components/SwiperCategory';
export default {
  data() {
    return {
      // screeWidth:0,
      tabnum:1,//交通指南切换
      rightlianxibig:1,//右下角联系
      erweima1:false,
      erweima2:false,
      days:'00',
      hours:'00',
      minutes:'00',
      seconds:'00',
    };
  },
  components: {
    SwiperDetail,
  },
  created(){
    setInterval(() => {
      let t1= moment();
      let t2 = moment('2020-10-16 00:00:00');
      let dura = t2.format('x') - t1.format('x');
      let tempTime = moment.duration(dura);
      let T = ''
      this.days = `${this.time(tempTime.days())}`
      this.hours = `${this.time(tempTime.hours())}`
      this.minutes = `${this.time(tempTime.minutes())}`
      this.seconds = `${this.time(tempTime.seconds())}`
    },1000)
  },
  beforeMount() {
    // this.screeWidth = window.screen.width
  },
  methods: {
    time(value) {
      if(value < 10){
        return `0${value}`
      } else {
        return value;
      }
    },
    tabBtn(a){
      if(a == 1){
        this.tabnum = 1
      }else{
        this.tabnum = 2
      }
    },
    lianxiMouseleave(a){
      console.log('jingru')
      if(a == 1){
        this.rightlianxibig = 2
      }else{
        this.rightlianxibig = 1
      }
    },
    lianxiMouseover(a){
      console.log('离开')
      setTimeout(() => {
        if(a == 2){
          this.rightlianxibig = 1
        }else{
          this.rightlianxibig = 2
        }  
      }, 1100);
    },
    erweima1Mousemove(){
      // this.rightlianxibig = 2
      this.erweima1 = true
    },
    erweima1Mouseout(){
      this.erweima1 = false
    },
    erweima2Mousemove(){
      this.erweima2 = true
    },
    erweima2Mouseout(){
      this.erweima2 = false
    },
  }
}
</script>

<style scoped>
.container {
  width: 100%;
  /* background-image: url(../assets/img/indexbg.png);
  background-size:100% 100%;  */
  min-width: 1400px;
  position: relative;
}
.indexbg{
  width: 100%;
  min-width: 1400px;
  height: 938px;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
.box{
  /* width: 1400px; */
  /* overflow: hidden; */
  position: relative;
  margin: auto;
}
.middle-box-one{
  margin: 0 auto;
  width: 100%;
  max-width: 1400px;
  /* height: 437px; */
  /* overflow: hidden; */
  border: 0px solid #ddd;
  display: flex;
  justify-content: space-between;
}
.middle-one-box-left{
  width: 394px;
}
.middle-one-box-right{
  display: flex;

}
.middle-one-box-right-item{
  display: block;
  padding: 0 26px;
  font-size: 18px;
  font-weight: 400;
  font-family: PingFangSC-Regular, PingFang SC;
  text-align: center;
}
.middle-one-box-right-item>img{
  display: block;
}

.middle-box-two{
  width: 100%;
  max-width: 1400px;
  margin: 667px auto 0;
  position: relative;
  z-index: 10;
  font-size: 46px;
  font-family: PingFang-SC-Heavy, PingFang-SC;
  font-weight: 800;
}
.middle-box-two-tian{
  position: absolute;
  left: 312px;
  top: 120px;
}
.middle-box-two-shi{
  position: absolute;
  left: 472px;
  top: 120px;
}
.middle-box-two-fen{
  position: absolute;
  left: 632px;
  top: 120px;
}
.middle-box-two-miao{
  position: absolute;
  left: 792px;
  top: 120px;
}
.index3-img{
  position: absolute;
  right: 23px;
  top: 51px;
  -webkit-animation-name: scaleDraw; /*关键帧名称*/
  -webkit-animation-timing-function: ease-in-out; /*动画的速度曲线*/
  -webkit-animation-iteration-count: infinite;  /*动画播放的次数*/
  -webkit-animation-duration: 4s; /*动画所花费的时间*/
}
@keyframes scaleDraw {  /*定义关键帧、scaleDrew是需要绑定到选择器的关键帧名称*/
  0%{
      transform: scale(1);  /*开始为原始大小*/
  }
  25%{
      transform: scale(1.1); /*放大1.1倍*/
  }
  50%{
      transform: scale(1);
  }
  75%{
      transform: scale(1.1);
  }
}
.middle-box-three{
  position: relative;
}
.middle-box-three-m{
  width: 100%;
  max-width: 1400px;
  margin: auto;
  overflow: hidden;
}
.index4-img{
  display: block;
  margin: 95px auto 50px;
}
.index5-img{
  width: 354px;
  position: absolute;
  top: -220px;
  left: 0;
  z-index: -1;
}
.index6-img{
  -webkit-transition:all 1s; 
  -moz-transition:all 1s;
  -o-transition:all 1s;
}
.index6-img:hover{
  -webkit-transform:scale(1.1); 
  -moz-transform:scale(1.1); 
  -o-transform:scale(1.1); 
}
.address{
  font-family: PingFangSC-Regular;
  font-size: 18px;
}
.middle-box-four{
  position: relative;
  margin: 94px 0 33px 0;
}
.index7-img{
  width: 100%;
  /* position: absolute;
  top: -0;
  left: 0;
  z-index: -1; */
}
.middle-box-five{
  
}
.middle-box-five-m{
  width: 100%;
  max-width: 1400px;
  margin: 0 auto 90px;
  display: flex;
  justify-content: space-between;
}
.middle-box-five-m-l{
  width: 610px;
  height: 340px;
  background: gainsboro;
}
.middle-box-five-m-r{
  width: 774px;

}
.middle-box-five-m-r-title{
  font-family: PingFangSC-Regular;
  font-size: 22px;
  line-height: 20px;
}
.middle-box-five-m-r-p{
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #666666;
  margin: 15px 0 0 0;
}
.middle-box-five-m-r-t-list{
  margin: 30px 0 0 0;
}
.middle-box-five-m-r-t-list-item{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 18px 0;
}
.middle-box-five-m-r-t-list-item-l{
  display: flex;
  align-items: center;
}
.middle-box-five-m-r-t-list-item-l > img{
  width: 12px;
  height: 16px;
}
.middle-box-five-m-r-t-list-item-l > h4{
  font-family: PingFangSC-Regular;
  font-size: 20px;
  color: #000000;
  margin:  0 0 0 8px;
}
.middle-box-five-m-r-t-list-item-r{
  font-family: PingFangSC-Regular;
  font-size: 20px;
  color: #666666;
}
.middle-box-six{
  position: relative;
}
.middle-box-six-m{
  position: relative;
  height: 1040px;
  width: 100%;
  max-width: 1400px;
  margin: auto;
}
.index9-img{
  width: 100%;
  height: 1040px;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
}
.index10-img{
  margin: auto;
  padding: 54px;
  display: block;
}
.jtnrzn-img{
  margin: 80px auto 0;
  display: block;
}
.middle-box-six-btn1{
  width: 172px;
  height: 46px;
  line-height: 46px;
  text-align: center;
  position: absolute;
  left: 0;
  top: 165px;
  border-radius: 23px;
  border: 1px solid #FFFFFF;
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #FFF;
}
.middle-box-six-btn2{
  width: 172px;
  height: 46px;
  line-height: 46px;
  text-align: center;
  position: absolute;
  left: 222px;
  top: 165px;
  border-radius: 23px;
  border: 1px solid #FFFFFF;
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #FFF;
}
.btn-active{
  color: #FF6E0A;
  border: 1px solid #FF6E0A;
}
.middle-box-six-adress{
  position: absolute;
  top: 484px;
  left: 0;
}
.middle-box-six-adress > h3{
  font-family: PingFang-SC-Heavy;
  font-size: 36px;
  color: #FFFFFF;
}
.middle-box-six-adress > p{
  font-family: PingFangSC-Regular;
  font-size: 22px;
  color: #FFFFFF;
}
.middle-box-six-adress1{
  top: 680px;
}
.middle-box-six-map{
  width: 879px;
  height: 610px;
  position: absolute;
  bottom: 110px;
  right: 26px;
  background: cornsilk;
}
.middle-box-seven{
  position: relative;
  height: 734px;
}
.index12-img{
  position: absolute;
  top: 0;
  right: 0;
}
.middle-box-seven-m{
  
}
.index13-img{
  width: 746px;
  height: 60px;
  display: block;
  margin: auto;
  padding: 93px 0 51px;
}
.middle-box-eight{
  position: relative;
}
.index14-img{
  width: 100%;
  height: 686px;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -1;
}
.middle-box-eight-m{
  height: 686px;
}
.index15-img{
  width: 238px;
  height: 60px;
  display: block;
  margin: auto;
  padding: 44px 0 0;
}
.middle-box-nine{
  position: relative;
}
.middle-box-nine-m{
  height: 635px;
}
.index17-img{
  width: 426px;
  position: absolute;
  left: 0;
  top: -84px;
  z-index: -2;
}
.index18-img{
  width: 602px;
  height: 60px;
  display: block;
  margin: auto;
  padding: 94px 0 51px;
}
.middle-box-nine-m-ping{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.middle-box-nine-m-ping > img{
  margin: 0 0 20px 0;
}
.ruzu-img{
  position: fixed;
  left: 0;
  top: 75%;
  z-index: 999;
}
/* 原来小图片 */
.lianxi-img{
  position: fixed;
  right: 0;
  bottom: 10%;
  z-index: 998;
}
.lianxibig-box{
  position: fixed;
  right: 0;
  bottom: 7%;
  z-index: 999;
}
.lianxibig-img{
  /* width: 160px;
  height: 418px; */
  width: 80px;
  height: 240px;
  opacity: 0;
  transition:width 1s,height 1s;
}
.lianxibig-img:hover{
  width:160px;
  height: 418px;
  opacity: 1;
}
.lianxibig-box-one{
  width: 160px;
  height: 100px;
  position: absolute;
  left: 0;
  top: 196px;
  z-index: 1000;
  /* background: forestgreen; */
}
/* .lianxibig-box-one:hover + .erweima1{
  opacity: 1;
} */
.lianxibig-box-two{
  width: 160px;
  height: 120px;
  position: absolute;
  left: 0;
  top: 297px;
  /* background: red; */
}
.erweima1{
  position: absolute;
  top: 95px;
  left: -160px;
  opacity: 0;
}
.erweima2{
  position: absolute;
  bottom: 25px;
  left: -160px;
}
</style>