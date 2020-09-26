<template>
  <div class="container">
    <Header/>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="i in 5">
          <img src="~/assets/img/tb1.png" alt="">
        </div>
      </div>
      <!-- Add Pagination -->
      <div class="swiper-pagination"></div>
    </div>

    <div class="talent-body">
      <div class="talent-body-left">
        <h4 class="title">职位类别</h4>
        <ul>
          <li>
            <input name="Fruit" type="checkbox" value=""/>
            <label>运营人员</label>
          </li>
          <li>
            <input name="Fruit" type="checkbox" value=""/>
            <label>安保经理</label>
          </li>
          <li>
            <input name="Fruit" type="checkbox" value=""/>
            <label>运营人员</label>
          </li>
          <li>
            <input name="Fruit" type="checkbox" value=""/>
            <label>安保经理</label>
          </li>
        </ul>
      </div>
      <div class="talent-body-right">
        <h3 class="r-title">开启新的工作</h3>

        <div class="content-box">
          <h3 class="content-item-h3">运营经理  职位月薪：4000-6000元</h3>
          <h4 class="content-item-h4">岗位职责：</h4>
          <p class="content-item-p">1、全面负责公司的安全保卫工作，按要求对园区安全进行检查，做好园区的三防（防火、防盗、防事故）工作，维护园区良好的生产生活秩序，保证园区安全；<br/>
                2、制定园区安保制度与计划，部署、督促、检查保安队的各项工作；<br/>
                3、制定保安队培训计划，定期对保安队进行业务培训；<br/>
                4、及时处理园区发生的突发事件，并及时报告上级主管；<br/>
                5、完成上级交办的其他任务。</p>
        </div>

        <div class="content-box">
          <h3 class="content-item-h3">运营经理  职位月薪：4000-6000元</h3>
          <h4 class="content-item-h4">岗位职责：</h4>
          <p class="content-item-p">1、全面负责公司的安全保卫工作，按要求对园区安全进行检查，做好园区的三防（防火、防盗、防事故）工作，维护园区良好的生产生活秩序，保证园区安全；<br/>
                2、制定园区安保制度与计划，部署、督促、检查保安队的各项工作；<br/>
                3、制定保安队培训计划，定期对保安队进行业务培训；<br/>
                4、及时处理园区发生的突发事件，并及时报告上级主管；<br/>
                5、完成上级交办的其他任务。</p>
        </div>

        <div class="content-box">
          <h3 class="content-item-h3">运营经理  职位月薪：4000-6000元</h3>
          <h4 class="content-item-h4">岗位职责：</h4>
          <p class="content-item-p">1、全面负责公司的安全保卫工作，按要求对园区安全进行检查，做好园区的三防（防火、防盗、防事故）工作，维护园区良好的生产生活秩序，保证园区安全；<br/>
                2、制定园区安保制度与计划，部署、督促、检查保安队的各项工作；<br/>
                3、制定保安队培训计划，定期对保安队进行业务培训；<br/>
                4、及时处理园区发生的突发事件，并及时报告上级主管；<br/>
                5、完成上级交办的其他任务。</p>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Swiper from 'swiper/js/swiper.min.js';
import 'swiper/css/swiper.min.css';
export default {
  mounted() {
    var swiper = new Swiper('.swiper-container', {
      loop: true,
      autoplay:true,
      pagination: {
        el: '.swiper-pagination',
      },
    });
  },
  methods: {

  },
}
</script>

<style scoped>
.swiper-container {
  width: 100%;
  height: 530px;
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
}
.swiper-slide > img{
  width: 100%;
  min-width: 1400px;
  height: 530px;
  object-fit: cover;
}
.talent-body{
  width: 100%;
  max-width: 1400px;
  margin: 90px auto 0;
  display: flex;
}
.talent-body-left > .title{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #000000;
  margin: 0 0 20px 0;
}
.talent-body-left{
  width: 240px;
}
.talent-body-left > ul{
  margin: 0 0 0 10px;
}
.talent-body-left > ul > li{
  display: flex;
  align-items: center;
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #000000;
  line-height: 30px;
}
.talent-body-left > ul > li > input{
  width: 18px;
  height: 18px;
  border-radius: 3px;
}
.talent-body-left > ul > li > input:checked{
  /* background: red; */
}
.talent-body-left > ul > li > label{
  padding: 0 0 0 10px;
}
.talent-body-right{
  width: 100%;
  border-left: 2px solid #DEDEDE;
  padding: 0 0 167px 40px;
}
.r-title{
  font-family: PingFang-SC-Bold;
  font-size: 22px;
  color: #000000;
}
.content-item-h3{
  font-family: PingFang-SC-Bold;
  font-size: 18px;
  color: #000000;
  margin: 40px 0 0 0;
}
.content-item-h4{
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #000000;
  margin: 10px 0 10px 0;
}
.content-item-p{
  font-family: PingFangSC-Regular;
  font-size: 18px;
  color: #333333;
}
</style>
