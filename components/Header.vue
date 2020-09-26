<template>
    <div class="header-box">
        <div class="header-box-m">
            <div class="middle-one-box-left">
                <img src="~/assets/img/logo.png" alt="" width="100%" >
            </div>
            <div class="middle-one-box-right">
                <nuxt-link class="middle-one-box-right-item" :to="{path: `/`}">
                <span>首页</span>
                </nuxt-link>
                <nuxt-link class="middle-one-box-right-item" :to="{path: `/about`}">
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
    </div>
</template>

<script>

export default {
  name: 'Header',
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
.header-box{
    height: 117px;
    width: 100%;
    position: relative;
    margin: auto;
}
.header-box-m{
    height: 117px;
    max-width: 1400px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
}
.middle-one-box-left{
  width: 394px;
}
.middle-one-box-right{
    height: 46px;
  display: flex;
  align-items: flex-start;
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
</style>
