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
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
              <span>展会专区</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
              <span>在线招商</span>
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
              商家展示
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
              新闻中心
            </nuxt-link>
            <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
              人才招聘
            </nuxt-link>
            <nuxt-link style="padding:0 0 0 20px" class="middle-one-box-right-item" :to="{path: `/about`}">
              关于我们
            </nuxt-link>
          </div>
        </div>

        <div class="middle-box-two">
          <img src="~/assets/img/index2.png" alt="">
          <div class="middle-box-two-tian">02</div>
          <div class="middle-box-two-shi">02</div>
          <div class="middle-box-two-fen">02</div>
          <div class="middle-box-two-miao">02</div>
          <img src="~/assets/img/index3.png" alt="" class="index3-img">
        </div>
        <img src="~/assets/img/index4.png" alt="" class="index4-img">

        <div class="middle-box-three">
          <img src="~/assets/img/index5.png" alt="" class="index5-img">
          <div class="middle-box-three-m">
            <img src="~/assets/img/index6.png" alt="">
            <div class="address">公司地址：河北廊坊胜芳国际家具博览中心</div>
          </div>
        </div>

        <div class="middle-box-four">
          <img src="@/assets/img/index7.png" alt="" class="index7-img">
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
                <div class="middle-box-five-m-r-t-list-item" v-for="i in 5">
                  <div class="middle-box-five-m-r-t-list-item-l">
                    <img src="@/assets/img/index8.png" alt="">
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
            <img src="@/assets/img/index10.png" alt="">
            <div class="middle-box-six-btn1 btn-active">实时地图</div>
            <div class="middle-box-six-btn2">交通图</div>
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
        </div>

        <div class="middle-box-seven">
          <img src="@/assets/img/index12.png" alt="" class="index12-img">
          <div class="common-middel middle-box-seven-m">
            <img src="@/assets/img/index13.png" alt="" class="index13-img">
          </div>
        </div>

        <div class="middle-box-eight">
          <img src="@/assets/img/index14.png" alt="" class="index14-img">
          <div class="common-middel middle-box-eight-m">
            <img src="@/assets/img/index15.png" alt="" class="index15-img">
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
        

      </div>
    <!-- </div> -->
    <Footer/>
  </div>
</template>
 
<script>
import Footer from '@/components/Footer';
export default {
  data() {
    return {
      // screeWidth:0,
    };
  },
  created(){
    
  },
  beforeMount() {
    // this.screeWidth = window.screen.width
  },
}
</script>

<style>
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
  height: 1030px;
}
.index9-img{
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.middle-box-six-m{
  width: 100%;
  max-width: 1400px;
  margin: auto;
}
.middle-box-six-m > img{
  margin: auto;
  padding: 54px;
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
  padding: 44px 0;
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
</style>
