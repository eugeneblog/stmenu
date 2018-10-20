<template>
    <div>
        <home-header :headerList="headerList"></home-header>
        <home-main :mainContext="mainContext"></home-main>
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
    this.getHomeInfo()
  }
}
</script>

<style scoped>
</style>
