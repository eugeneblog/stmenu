<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        {{ context.title }}
                    </div>
                    <div class="header_detail">
                        {{ context.detail }}
                    </div>
                    <div class="header_more_feature">
                        <el-row>
                            <el-col
                            :xs="12" :sm="12" :md="12" :lg="12" :xl="12"
                            v-for="item in colFeature"
                            :key="item.id"
                            >
                                <div class="grid-content bg-purple">
                                    <div
                                    class="header_more_feature_item__content"
                                    v-for="text of item.feature"
                                    :key="text.id">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                           {{ text.text }}
                                        </div>
                                    </div>
                                </div>
                            </el-col>
                        </el-row>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderFeatureMore',
  data () {
    return {
      context: {
        title: 'S-Token标准加密资产合规的基石',
        detail: 'S-Token是一个开源标准，是Stmenu Compliance协议的核⼼部分。S-Token在每个步骤和跨辖区(从发行到交易)都符合法规。',
        feature: [
          {
            id: 1,
            text: 'ERC-1400兼容并与现有的以太坊⽣态系统协同⼯作'
          }, {
            id: 2,
            text: '转帐只能在满⾜交易条件的白名单之间进行'
          }, {
            id: 3,
            text: '灵活的框架，以执行证券法规、KYC / AML政策、税收规则等。'
          }, {
            id: 4,
            text: ' 在token级别跨交易平台遵从各国家/区域合规性'
          }
        ]
      }
    }
  },
  computed: {
    colFeature () {
      let len = this.context.feature.length
      let arr = []
      for (let i = 1; i <= len / 2; i++) {
        let o = {}
        o.id = i
        o.feature = this.context.feature.slice(i * 2 - 2, i * 2)
        arr.push(o)
      }
      return arr
    }
  }
}
</script>

<style lang="scss" scoped>
.el-row {
    background: #ffffff;
    background-repeat: no-repeat;
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
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .index__leftSlashes{
    position: absolute;
    left: 0;
    bottom: 0;
    width: 275px;
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
    margin: 0 auto;
    color: #727988;
    margin-top: 16px;
    font-weight: 300;
    text-align: center;
    line-height: 1.75;
  }
  .header_more_feature {
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    flex-wrap: wrap;
    margin-top: 43px;
    margin-bottom: 28px;
    width: 100%;
  }
  .header_more_feature .header_more_feature_item__content {
      padding-right: 24px;
      line-height: 2;
  }
  .header_more_feature .header_more_feature_item__content > i {
      display: block;
      width: 34px;
      height: 34px;
      line-height: 34px;
      font-weight: 800;
      float: left;
      font-size: 20px;
      margin-right: 20px;
      background: #a1dcd4;
      color: #ffffff;
      text-align: center;
      border-radius: 50%;
  }
  .header_more_feature .header_more_feature_item__content > .header_more_feature_item__text {
      float: left;
      margin-bottom: 10px;
      width: 80%;
  }
  @media screen and (max-width: 760px) {
     .el-col-xs-12{
         width: 100%;
     }
     .el-col-md-12{
         width: 100%;
     }
     .el-col-sm-12{
         width: 100%;
     }
     .el-col-xl-12{
         width: 100%;
     }
     .header_more_feature_item__text {
         font-size: 14px;
         width: 100%;
     }
     .header_more_feature .header_more_feature_item__content > i {
         width: 24px;
         height: 24px;
         line-height: 24px;
         margin-right: 10px;
         font-size: 14px;
     }
  }
</style>
