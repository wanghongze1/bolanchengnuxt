<template>
  <div class="footer-box">
      <div class="xian"></div>
      <div class="common-middel footer-box-m">
          <div class="footer-box-m-t">
              <p>友情链接：</p>
              <a target="_blank" href="http://www.sffa.cn/index.html">胜芳家协</a>
              <a target="_blank" href="http://www.sfdzh.com/">胜芳大杂烩</a>
          </div>
          <div class="footer-box-m-b">
              <p>电话:0316-7896115 Email:service@sf-ifc.com 胜芳家具,家具展会,家具批发 请选择胜芳国际家具博览城 ICP证：冀ICP备14005185号-1</p>
              <p>Copyright © 2005 - 2020 www.sf-ifc.com All Rights Reserved 版权所有：胜芳国际家具博览城 地址：河北省廊坊市胜芳镇政府北行</p>
              <p>违法和不良信息举报电话举报电话：0316-7896115 违法和不良信息举报邮箱：sf_ifc@126.com</p>
          </div>
      </div>
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
    background: url(https://hongshuye01.oss-cn-beijing.aliyuncs.com/mall/banner/image/20200906/b84550f348b54adea5ec593b9aaf48fc.png);
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
.footer-box-m-b{
    font-family: PingFang-SC-Bold;
    font-size: 14px;
    color: #FFFFFF;
    line-height: 36px;
    text-align: center;
    margin: 55px 0 0 0;
}
</style>
