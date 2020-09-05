<template>
  <div class="footer-box">
      <div class="xian"></div>
      <div class="common-middel footer-box-m">
          <div class="footer-box-m-t">
              <p>友情链接：</p>
              <a target="_blank" href="http://www.sffa.cn/index.html">胜芳家协</a>
              <a target="_blank" href="http://www.sfdzh.com/">胜芳大杂烩</a>
              
          </div>
          
      </div>
    <!-- <div class="footer-cont-list">
      <a :href="`${curCity}/aboutus`">关于我们</a>
      <a :href="`${curCity}/guanqihui`">企业租房</a>
      <a href="http://www.longfor.com/">龙湖集团</a>
    </div>
    <p class="phone">
      400-001-1166
    </p>
    <p class="copy-right">
      Copyright 2018 冠寓版权所有 冠寓商业管理有限公司
      <br/>
      <a target="_blank" href="http://www.beian.miit.gov.cn/">京ICP备17060342号</a>
    </p> -->
  </div>
</template>

<script>

export default {
  name: 'Footer',
  props: {
    
  },
  data() {
    return {

    }
  },
  mounted() {

  },
  methods: {

  },
}
</script>

<style scoped>
.footer-box{
    width: 100%;
    height: 417px;
    background: url(../assets/img/footer.png);
    background-size: 100% 417px;
    position: relative;
}
.xian{
    height: 1px;
    width: 100%;
    background: #FFFFFF;
    position: absolute;
    top: 140px;
    left: 0;
}
.footer-box-m{
    
}
.footer-box-m-t{
    height: 140px;
    display: flex;
    align-items: center;
    font-family: PingFang-SC-Bold;
    color: #FFFFFF;
}
.footer-box-m-t > p{
    font-size: 20px;
}
.footer-box-m-t > a{
    font-size: 16px;
    color: #ccc;
    padding: 0 0 0 60px;
}
</style>
