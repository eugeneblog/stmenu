<template>
    <div>
        <home-header></home-header>
        <home-main></home-main>
        <header-main-description></header-main-description>
        <header-feature></header-feature>
        <header-feature-more></header-feature-more>
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
import HomeExample from './commpoents/HomeExample'
import HomeFooter from './commpoents/HomeFooter'
import HomeFooterInformation from './commpoents/HomeFooterInformation'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeMain,
    HeaderMainDescription,
    HeaderFeature,
    HeaderFeatureMore,
    HomeExample,
    HomeFooter,
    HomeFooterInformation
  }
}
</script>

<style scoped>

</style>
