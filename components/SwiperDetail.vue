<template>
  <div id="SwiperDetail">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img src="~/assets/img/swiper/certify01.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="~/assets/img/swiper/certify02.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="~/assets/img/swiper/certify03.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="~/assets/img/swiper/certify04.png" alt="">
        </div>
      </div>
    </div>
    <!-- <div class="swiper-pagination"></div> -->
		<div class="swiper-button-prev"></div>
		<div class="swiper-button-next"></div>
  </div>
  
</template>
<script>
  import Swiper from 'swiper/js/swiper.min.js';
  import 'swiper/css/swiper.min.css';

  export default {
    layout: 'SwiperDetail',
    head() {},
    data() {
      return {

      };
    },
    computed: {},
    beforeMount() {

    },
    mounted() {
      const swipeSwiperDetailrTitle = new Swiper('#SwiperDetail .swiper-container', {
        watchSlidesProgress: true,
        slidesPerView: 'auto',
        centeredSlides: true,
        loop: true,
        autoplay: false,
        loopedSlides: 5,
        navigation: {
          nextEl: '#SwiperDetail .swiper-button-next',
          prevEl: '#SwiperDetail .swiper-button-prev',
        },
        on: {
          progress: function (progress) {
            for (let i = 0; i < this.slides.length; i++) {
              var slide = this.slides.eq(i);
              var slideProgress = this.slides[i].progress;
              let modify = 1;
              if (Math.abs(slideProgress) > 1) {
                modify = (Math.abs(slideProgress) - 1) * 0.3 + 1;
              }
              let translate = slideProgress * modify * 260 + 'px';
              let scale = 1 - Math.abs(slideProgress) / 5;
              let zIndex = 999 - Math.abs(Math.round(10 * slideProgress));
              slide.transform('translateX(' + translate + ') scale(' + scale + ')');
              slide.css('zIndex', zIndex);
              slide.css('opacity', 1);
              if (Math.abs(slideProgress) > 3) {
                slide.css('opacity', 0);
              }
            }
          },
          setTransition: function (transition) {
            for (let i = 0; i < this.slides.length; i++) {
              var slide = this.slides.eq(i)
              slide.transition(transition);
            }

          }
        }
      })
    },
    methods: {

    },
  };

</script>
<style>
#SwiperDetail {
  position: relative;
  width: 90%;
  margin: 0 auto;
}

#SwiperDetail .swiper-container {
  padding-bottom: 60px;
}

#SwiperDetail  .swiper-slide {
  width: 660px;
  height: 440px;
  background: #fff;
}
#SwiperDetail  .swiper-slide img{
  display:block;
  width: 100%;
}
#SwiperDetail  .swiper-slide p {
  line-height: 98px;
  padding-top: 0;
  text-align: center;
  color: #636363;
  font-size: 1.1em;
  margin: 0;
}
#SwiperDetail .swiper-button-prev {
  top: 37%;
  left: 31px;
  width: 38px;
  height: 72px;
  outline: none;
  background: url('../assets/img/swiper/sl.png') no-repeat;
  /* background-position: 0 0; */
  background-size: 100%;
}
#SwiperDetail .swiper-button-next {
  top: 37%;
  right: 31px;
  width: 38px;
  height: 72px;
  outline: none;
  background: url('../assets/img/swiper/sr.png') no-repeat;
  /* background-position: 0 -93px; */
  background-size: 100%;
}
.swiper-button-prev:after, .swiper-container-rtl .swiper-button-next:after{
  content: '';
}
.swiper-button-next:after, .swiper-container-rtl .swiper-button-prev:after{
  content: '';
}
</style>
