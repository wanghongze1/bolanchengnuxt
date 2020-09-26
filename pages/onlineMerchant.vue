<template>
  <div class="container">
    <Header/>
    <div class="zhaoshang-box">
      <div class="zhaoshang-box-one">
        <img src="~/assets/img/zhaoshangbanner.png" alt="" class="zhaoshangbanner" >
        <div class="zhaoshang-box-one-m">
          <div class="text-one">Investment consultant</div>
          <div class="text-two">招商顾问</div>
          <div class="swiper-container">
            <div class="swiper-wrapper">
              <div class="swiper-slide" v-for="i in 10">
                <img src="~/assets/img/shang.png" alt="" class="guwen-touxaing">
                <div class="guwen-r-box">
                  <div class="guwen-name">郑燕</div>
                  <div class="guwen-zhiwei">A馆主管  招商负责人</div>
                  <div class="guwen-phone">
                    <img class="guwen-phone-icon" src="~/assets/img/phone.png" alt="">
                    <p class="guwen-phone-text">18888888888</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-button-next"></div>
          <div class="swiper-button-prev"></div>
        </div>
      </div>

      <div class="zhaoshang-box-two">
        <div class="zhaoshang-box-two-m">
          <div class="zhaoshang-item-tab zhaoshang-item-tab-active">馆内商铺</div>
          <div class="zhaoshang-item-tab">材料城商铺</div>
          <div class="zhaoshang-item-tab">小吃街摊位</div>
          <div class="zhaoshang-item-tab">材料展位</div>
        </div>
      </div>

      <div class="zhaoshang-box-three">
        <div class="zhaoshang-box-three-m">
          <div class="zhaoshang-box-three-m-item" v-for="i in 9">
            <img src="~/assets/img/tu1.png" alt="" class="zhaoshang-box-three-m-item-img">
            <h3 class="three-weizi">位置：A8-990</h3>
            <div class="three-name">招商顾问：郑燕</div>
            <div class="three-name">联系电话：18888888888</div>
            <div class="three-see">查看详情</div>
          </div>
        </div>
      </div>
      <div style="height:90px;"></div>
      
    </div>

    <div class="xuanfu-box">
      <div class="xuanfu-one">您想租赁什么样的展位</div>
      <div class="xuanfu-two">
        <!-- <input type="text" placeholder="请选择家具分类"> -->
        <select class="xuanfu-two-select" >
          <option value="请选择家具分类">请选择家具分类</option>
          <option value="volvo">Volvo</option>
          <option value="saab">Saab</option>
          <option value="opel">Opel</option>
          <option value="audi">Audi</option>
        </select>
        <!-- <img class="xuanfu-two-img" src="~/assets/img/fenleiicon.png" alt=""> -->
      </div>
      <div class="xuanfu-two">
        <input class="xuanfu-two-input" type="text" placeholder="期望租赁展位面积">
        <img class="xuanfu-two-img" src="~/assets/img/mianjiicon.png" alt="">
      </div>
      <div class="xuanfu-two">
        <input class="xuanfu-two-input" type="text" placeholder="您的联系手机">
        <img class="xuanfu-two-img" src="~/assets/img/phoneicon.png" alt="">
      </div>
      <textarea class="xuanfu-two-beizhu" name="" id="" cols="30" rows="10" placeholder="备注："></textarea>
      <div class="xuanfu-submit">提交</div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Swiper from 'swiper/js/swiper.min.js';
import 'swiper/css/swiper.min.css';
export default {
  mounted() {
    const SwiperCategory = new Swiper('.swiper-container', {
      slidesPerView: 4,
      spaceBetween: 50,
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    });
  },
  methods: {

  },
}
</script>

<style scoped>
.zhaoshang-box{
  width: 100%;
  min-width: 1400px;
}
.zhaoshang-box-one{
  width: 100%;
  min-width: 1400px;
  height: 680px;
  position: relative;
}
.zhaoshangbanner{
  width: 100%;
  min-width: 1400px;
  height: 680px;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  object-fit: cover;
}
.zhaoshang-box-one-m{
  margin: auto;
  width: 100%;
  height: 680px;
  max-width: 1400px;
  /* background: #fff; */
  position: relative;
}
.swiper-container {
  width: 90%;
  height: 114px;
  /* background: crimson; */
  padding: 506px 0 0 0;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
  display: flex;
}
.swiper-button-prev {
    top: 81%;
    left: 0;
    width: 38px;
    height: 72px;
    outline: none;
    background: url('../assets/img/swiper/ljt.png') no-repeat;
    background-size: 100%;
  }
.swiper-button-next {
  top: 81%;
  right: 0;
  width: 38px;
  height: 72px;
  outline: none;
  background: url('../assets/img/swiper/rjt.png') no-repeat;
  background-size: 100%;
}
.text-one{
  position: absolute;
  left: 5%;
  top: 430px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #FFFFFF;
  text-shadow: 0 1px 0 rgba(0,0,0,0.50);
}
.text-two{
  position: absolute;
  left: 5%;
  top: 454px;
  font-family: PingFang-SC-Bold;
  font-size: 22px;
  color: #FFFFFF;
  text-shadow: 0 2px 0 rgba(0,0,0,0.65);
}
.guwen-touxaing{
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin: 17px 20px 17px 33px;
}
.guwen-r-box{
  display: flex;
  flex-wrap: wrap;
}
.guwen-name{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #000000;
}
.guwen-zhiwei{
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #000000;
  margin: 8px 0 14px;
}
.guwen-phone{
  display: flex;
  align-items: center;
}
.guwen-phone-icon{
  width: 14px;
  height: 18px;
  padding: 0 8px 0 0;
}
.guwen-phone-text{
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #000000;
}
.zhaoshang-box-two{
  width: 100%;
  min-width: 1400px;
  height: 100px;
  border-bottom: 1px solid #DEDEDE;
  background: #FBFBFB;
}
.zhaoshang-box-two-m{
  margin: auto;
  width: 100%;
  height: 100px;
  max-width: 1400px;
  position: relative;
  display: flex;
}
.zhaoshang-item-tab{
  margin: 0 70px 0 0;
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #333333;
  padding: 40px 0 30px;
}
.zhaoshang-item-tab-active{
  color: #000;
  border-bottom:  3px solid #B71C22;
}
.zhaoshang-box-three{
  width: 100%;
  min-width: 1400px;
  background: #FBFBFB;
}
.zhaoshang-box-three-m{
  margin: auto;
  width: 100%;
  max-width: 1400px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 0 0 90px 0;
}
.zhaoshang-box-three-m-item{
  width: 448px;
  position: relative;
  margin: 90px 0 0 0;
}
.zhaoshang-box-three-m-item-img{
  width: 448px;
  height: 252px;
}
.three-weizi{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #000000;
  margin: 24px 0 14px;
}
.three-name{
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #333333;
}
.three-see{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #FFFFFF;
  background: #FFA91F;
  width: 120px;
  height: 37px;
  line-height: 37px;
  text-align: center;
  position: absolute;
  bottom: 24px;
  right: 0;
}
.zhaoshang-box-three-m:after {
    content: "";
    width: 448px;
}
.xuanfu-box{
  width: 190px;
  height: 288px;
  background: #FFFFFF;
  box-shadow: 0 2px 10px 0 rgba(0,0,0,0.27);
  position: fixed;
  left: 0;
  bottom: 10%;
  z-index: 999;
}
.xuanfu-one{
  width: 100%;
  height: 36px;
  line-height: 36px;
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #FFFFFF;
  background: #F9901F;
  text-align: center;
}
.xuanfu-two{
  width: 170px;
  height: 30px;
  margin: 10px auto 0;
  border: 1px solid #C6C6C6;
  border-radius: 4px;
  border-radius: 4px;
  display: flex;
  align-items: center;
}
.xuanfu-two-input{
  border: 0;
  padding: 6px 8px;
  width: 132px;
  outline:none;
}
.xuanfu-two-select{
  border: 0;
  padding: 6px 8px;
  width: 170px;
  outline:none;
  appearance:none;  
  -moz-appearance:none;  
  -webkit-appearance:none;  
  background: url("../assets/img/fenleiicon.png") no-repeat 170px center;  
  background-size: 14px;
  background-position: 148px 8px;
  cursor: pointer;
}
.xuanfu-two-img{
  width: 14px;
  height: 14px;
}
.xuanfu-two-beizhu{
  width: 156px;
  height: 54px;
  margin: 10px 10px 5px;
  border: 1px solid #C6C6C6;
  outline:none;
  padding: 6px;
  resize: none;
  border-radius: 4px;
}
.xuanfu-submit{
  width: 170px;
  height: 30px;
  line-height: 30px;
  text-align: center;
  background: #FF7800;
  border-radius: 4px;
  margin: auto;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #FFFFFF;
}
</style>