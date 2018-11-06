<template>
    <div>
        <home-header :headerList="headerList"></home-header>
        <home-main ref="homeMain" :mainContext="mainContext"></home-main>
        <header-main-description :mainDescription="mainDescription"></header-main-description>
        <header-feature :homeFeatureContext="HomeFeatureContext"></header-feature>
        <header-feature-more></header-feature-more>
        <header-feature-des></header-feature-des>
        <home-example></home-example>
        <home-footer></home-footer>
        <home-footer-information></home-footer-information>
    </div>
</template>

<script>
import HomeHeader from './commpoents/HomeHeader'
import HomeMain from './commpoents/HomeMain'
import HeaderMainDescription from './commpoents/HeaderMainDescription'
import HeaderFeature from './commpoents/HeaderFeature'
import HeaderFeatureMore from './commpoents/HeaderFeatureMore'
import HeaderFeatureDes from './commpoents/HeaderFeatureDes'
import HomeExample from './commpoents/HomeExample'
import HomeFooter from './commpoents/HomeFooter'
import HomeFooterInformation from './commpoents/HomeFooterInformation'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeMain,
    HeaderMainDescription,
    HeaderFeature,
    HeaderFeatureMore,
    HeaderFeatureDes,
    HomeExample,
    HomeFooter,
    HomeFooterInformation
  },
  data () {
    return {
      headerList: {},
      mainContext: {},
      mainDescription: {},
      HomeFeatureContext: {}
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('static/mock/homeData.json').then(this.getHomeInfoSuc)
    },
    getHomeInfoSuc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.headerList = data.headerList
        this.mainContext = data.mainContext
        this.mainDescription = data.mainDescription
        this.HomeFeatureContext = data.HomeFeatureContext
      }
    }
  },
  mounted () {
    const _this = this
    let mainBg = _this.$refs.homeMain.$el
    this.getHomeInfo()
    let top = -380
    let scrollFunc = function (e) {
      e = e || window.event
      if (e.wheelDelta) { // 第一步：先判断浏览器IE，谷歌滑轮事件
        if (e.wheelDelta > 0) { // 当滑轮向上滚动时
          mainBg.style.backgroundPosition = `50% ${top}px`
          if (top > -448) {
            top -= 0.8
          }
        }
        if (e.wheelDelta < 0) { // 当滑轮向下滚动时\
          mainBg.style.backgroundPosition = `50% ${top}px`
          if (top < -350) {
            top = top + 0.8
          }
        }
      } else if (e.detail) { // Firefox滑轮事件
        if (e.detail > 0) {
          mainBg.style.backgroundPosition = `50% ${top}px`
          if (top > -448) {
            top -= 0.8
          }
        }
        if (e.detail < 0) { // 当滑轮向下滚动时
          mainBg.style.backgroundPosition = `50% ${top}px`
          if (top < -350) {
            top = top + 0.8
          }
        }
      }
    }
    // 给页面绑定滑轮滚动事件
    if (document.addEventListener) { // firefox
      document.addEventListener('DOMMouseScroll', scrollFunc, false)
    }
    // 滚动滑轮触发scrollFunc方法  // ie 谷歌
    window.onmousewheel = document.onmousewheel = scrollFunc
  }
}
</script>

<style scoped>
</style>
