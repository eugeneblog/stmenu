<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        {{ HomeFeatureContext.title }}
                    </div>
                    <div class="header_detail">
                        {{ HomeFeatureContext.detail }}
                    </div>
                    <div class="header_feature_content">
                        <div
                        class="header_feature_item"
                        v-for="item in HomeFeatureContext.feture"
                        :key='item.id'
                        >
                            <div class="header_feature_item_title">{{ item.title }}</div>
                            <ul v-for="text of item.texts" :key='text.id'>
                                <li>{{ text.text }}</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderFeature',
  props: {
    HomeFeatureContext: Object
  }
}
</script>

<style lang="scss" scoped>
.el-row {
    background: #eaf6fb;
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .index__leftSlashes{
    position: absolute;
    left: 0;
    bottom: 0;
  }
  .header_title {
    margin-top: 80px;
    width: 100%;
    font-size: 32px;
    text-align: center;
    color: #1b1d2e;
    line-height: 64px;
    font-weight: 300;
  }
  .header_detail {
    font-size: 16px;
    max-width: 980px;
    margin: 0 auto;
    color: #727988;
    margin-top: 16px;
    font-weight: 300;
    text-align: center;
    line-height: 1.75;
  }
  .header_feature_content {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      width: 100%;
      flex-direction: row;
      margin: 32px 0 60px 22px;
  }
  .header_feature_content .header_feature_item{
      margin-top: 40px;
      width:33.33%;
      text-align: left;
      float: left;
  }
  .header_feature_content .header_feature_item ul {
      font-size: 16px;
      color: #727988;
      font-weight: 300;
      padding: 0px;
  }
  .header_feature_content .header_feature_item ul>li {
      position: relative;
      list-style: none;
      display: list-item;
      margin-top: 12px;
      padding-left: 20px;
  }
  .header_feature_content .header_feature_item ul>li:before{
    display: block;
    position:absolute;
    left: -2px;
    top: 6px;
    margin-right: 12px;
    content: " ";
    width: 10px;
    height: 10px;
    background: #2040a0;
    border-radius: 50%;
    font-family: FontAwesome;
    line-height: 28px;
  }
   @media screen and (max-width: 760px) {
       .header_feature_content{
           flex-direction: column;
       }
       .header_feature_content .header_feature_item {
           width: 90%;
       }
   }
</style>
