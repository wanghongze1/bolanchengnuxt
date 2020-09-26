<template>
  <div id="SwiperCategory">
    
    <div class="swiper-container">
      <div style="height:50px;"></div>
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="i in 10">
          <div class="yingying"></div>
          <!-- <img src="@/assets/img/ping7.png" alt="" class="swiper-slide-img"> -->
          <img src="@/assets/img/ping7.png" alt="" class="swiper-slide-img-p">
          <p class="swiper-slide-a swiper-slide-p">椅子</p>
        </div>
      </div>

      <div class="swiper-pagination"></div>

      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </div>
  </div>

</template>
<script>
  import Swiper from 'swiper/js/swiper.min.js';
  import 'swiper/css/swiper.min.css';

  export default {
    mounted() {
      const SwiperCategory = new Swiper('#SwiperCategory .swiper-container', {
        slidesPerView: 5,
        spaceBetween: 50,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        navigation: {
          nextEl: '#SwiperCategory .swiper-button-next',
          prevEl: '#SwiperCategory .swiper-button-prev',
        },
      });
    },
    methods: {

    },
  };

</script>
<style>
  #SwiperCategory {
    position: relative;
    /* width: 90%; */
    margin: 0 auto;
  }
  #SwiperCategory .swiper-container {
    width: 100%;
    height: 500px;
  }
  #SwiperCategory .swiper-slide {
    position: relative;
    width: 240px !important;
    height: 330px;
    text-align: center;
    font-size: 18px;
    background: #fff;
    box-shadow: 0 0 14px 0 rgba(0,0,0,0.20);
    -webkit-transition:all 0.5s; 
    -moz-transition:all 0.5s;
    -o-transition:all 0.5s;
  }
  #SwiperCategory .swiper-slide:hover{
    -webkit-transform:scale(1.1); 
    -moz-transform:scale(1.1); 
    -o-transform:scale(1.1); 
  }
  #SwiperCategory .swiper-slide .yingying{
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100%;
    opacity: 0.62;
    background: #000000;
  }
  .swiper-pagination-bullet-active{
    background: #B71C22;
  }
  #SwiperCategory .swiper-button-prev {
    top: 85%;
    left: 0;
    width: 60px;
    height: 30px;
    outline: none;
    background: url('../assets/img/swiper/lj.png') no-repeat;
    background-size: 100%;
  }
  #SwiperCategory .swiper-button-next {
    top: 85%;
    right: 0;
    width: 60px;
    height: 30px;
    outline: none;
    background: url('../assets/img/swiper/rj.png') no-repeat;
    background-size: 100%;
  }
  #SwiperCategory .swiper-pagination-bullet{
    width: 14px;
    height: 14px;
  }
  .swiper-slide-img-p{
    width: 100%;
    height: 250px;
    display: block;
  }
  .swiper-slide-a{
    height: 80px;
    line-height: 80px;
    font-family: PingFangSC-Regular;
    font-size: 20px;
    color: #000000;
  }
  .swiper-slide-img-p{
    position: absolute;
    top: 0;
    left: 0;
    width: 100% !important;
    height: 100% !important;

  }
  .swiper-slide-p{
    height: 350px !important;
    line-height: 350px !important;
    position: relative;
    z-index: 2;
    font-family: PingFangSC-Regular;
    font-size: 22px;
    color: #FFFFFF;
  }
</style>
