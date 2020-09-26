<template>
  <div class="container">
    <Header />
    <section class="banner-wrap"></section>
    <nav class="nav-wrap">
      <vue-tabs @tab-change="handleTabChange">
        <v-tab title="公司动态">
          <div class="card-wrap"></div>
          <div class="card-drift"></div>
        </v-tab>
        <v-tab title="行业资讯">
          行业资讯
        </v-tab>
        <v-tab title="媒体报道">
          媒体报道
        </v-tab>
        <v-tab title="视频中心">
          视频中心
        </v-tab>
      </vue-tabs>
    </nav>
    <aside class="dynamic-container">
      <ul class="dynamic-list">
        <li class="ks-clear">
          <div class="title">
            胡桃木家具设计风格
          </div>
          <div class="date">
            06-23
          </div>
        </li>
        <li class="ks-clear">
          <div class="title">
            胡桃木家具设计风格
          </div>
          <div class="date">
            06-23
          </div>
        </li>
        <li class="ks-clear">
          <div class="title">
            胡桃木家具设计风格
          </div>
          <div class="date">
            06-23
          </div>
        </li>
        <li class="ks-clear">
          <div class="title">
            胡桃木家具设计风格
          </div>
          <div class="date">
            06-23
          </div>
        </li>
        <li class="ks-clear">
          <div class="title">
            胡桃木家具设计风格
          </div>
          <div class="date">
            06-23
          </div>
        </li>
      </ul>
      <paginate
        :page-count="1467"
        :page-range="5"
        :margin-pages="3"
        :click-handler="clickCallback"
        :prev-text="'<'"
        :next-text="'>'"
        :container-class="'pagination'"
        :page-class="'page-item'"
      >
      </paginate>
    </aside>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Paginate from "vuejs-paginate";
import { VueTabs, VTab } from "vue-nav-tabs";
// https://github.com/lokyoung/vuejs-paginate   分页
// https://github.com/bhuh12/vue-router-tab 路由tabs
// https://github.com/cristijora/vue-tabs tabs
import axios from "axios";
export default {
  components: {
    Paginate,
    VueTabs,
    VTab
  },
  head() {
    return {
      title: '新闻中心',
      meta: [{ hid: "description", name: "新闻中心", content: "新闻中心" }]
    };
  },
  data() {
    return {};
  },
  created() {},
  beforeMount() {},
  methods: {
    clickCallback(pageNum) {
      console.log(pageNum);
    },
    handleTabChange(tabIndex, newTab, oldTab) {
      //your code here
    }
  }
  // async asyncData() {
  //   let { data } = await axios.get("https://api.myjson.com/bins/8gdmr");
  //   return { info: data };
  // }
};
</script>

<style scoped>
.banner-wrap {
  width: 100%;
  height: 100%;
  max-width: 1920px;
  max-height: 530px;
  min-width: 1400px;
  min-height: 386.4583px;
  margin: 0 auto;
  background: url("~assets/img/tu1.png") center/cover no-repeat;
}

.nav-wrap {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  font-size: 18px;
  color: #333333;
  letter-spacing: 0;
}

.nav-wrap /deep/ .nav-tabs {
  border-bottom: 2px solid #dedede;
}

.nav-wrap /deep/ .nav-tabs .tab {
  display: inline-block;
  padding: 30px 0;
  box-sizing: border-box;
}

.nav-wrap /deep/ .nav-tabs .tab a {
  color: #333333;
}
.nav-wrap /deep/ .nav-tabs .active a {
  color: #000;
}

.nav-wrap /deep/ .nav-tabs .tab + .tab {
  margin-left: 40px;
}

.nav-wrap /deep/ .nav-tabs li.active {
  border-bottom: 2px solid #b71c22;
}

.nav-wrap /deep/ .tab-content {
  position: relative;
  padding: 95px 0 20px;
}

.nav-wrap .card-wrap {
  width: 100%;
  height: 393px;
  background: #1c2024;
}

.nav-wrap .card-drift {
  position: absolute;
  width: 394px;
  height: 520px;
  background: url("~assets/img/tu1.png") center/cover no-repeat;
  top: calc(50% - 230px);
  right: 3%;
}

.dynamic-container {
  width: 100%;
  max-width: 1400px;
  margin: 30px auto 50px;
}

.dynamic-container .dynamic-list {
  font-size: 20px;
  color: #000000;
  height: 460px;
}

.dynamic-container .dynamic-list li::before {
  float: left;
  content: "";
  width: 0;
  height: 0;
  border: 10px solid transparent;
  border-left-color: #b71c22;
  margin-top: 5px;
}

.dynamic-container .dynamic-list .title {
  float: left;
}

.dynamic-container .dynamic-list .date {
  float: right;
  color: #666;
}

.dynamic-container .dynamic-list li {
  margin-top: 40px;
}

.dynamic-container /deep/ .pagination {
  margin-top: 50px;
}

.dynamic-container /deep/ .pagination li {
  display: inline-block;
  font-size: 16px;
}

.dynamic-container /deep/ .pagination li + li {
  margin-left: 18px;
}

.dynamic-container /deep/ .pagination li a {
  color: #606266;
}

.dynamic-container /deep/ .pagination .active a {
  color: #b71c22;
  border: none;
  overflow: hidden;
}
.dynamic-container /deep/ .pagination .active a:focus {
  outline-style: none;
  -moz-outline-style: none;
}
</style>
