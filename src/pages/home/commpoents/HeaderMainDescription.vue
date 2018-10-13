<template>
    <div>
        <el-row :gutter="20">
            <el-col :xs="0" :sm="1" :md="1" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
            <el-col :xs="12" :sm="11" :md="11" :lg="6" :xl="11">
                <div class="grid-content bg-purple-light">
                    <div class="grid-content-box">
                        <div class="index__opportunityDots">
                            <img :src='context.imgUrl.blockchain'>
                        </div>
                        <pre class="index__opportunityTitle" >{{ context.title }}</pre>
                    </div>
                </div>
            </el-col>
            <el-col :xs="12" :sm="11" :md="11" :lg="10" :xl="11">
                <div class="grid-content">
                    <div class="grid-context">
                        <p
                        v-for="item in context.detail"
                        :key="item.id"
                        :class="item.class">{{ item.text }}</p>
                    </div>
                </div>
            </el-col>
            <el-col :xs="0" :sm="1" :md="1" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderMainDescription',
  data () {
    return {
      context: {
        imgUrl: {
          blockchain: 'https://harbor.com/images/index/opportunity/blockchain-three-dots.svg'
        },
        title: `改变财产观念，资产数字化是未来趋势。`,
        detail: [
          {
            id: 1,
            class: 'index__opportunityResponse1',
            text: '资产TOKEN化是将资产权益转换为区块链上token的过程，从而使资本形成更快，更容易和更方便转变为颗粒化财产形态，同时为投资者释放二级流动性和价值'
          }, {
            id: 2,
            class: 'index__opportunityResponse2',
            text: 'Stmenu平台和合规协议确保令牌化证券符合发行时的现有证券法以及全球各地的每笔交易。'
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.el-row {
    background: #f6f6f6;
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
  .grid-content-box {
      overflow: hidden;
      word-wrap: break-word;
    margin-left: 40px;
  }
  .index__opportunityDots {
      margin-top: 59px;
  }
  .grid-context {
      margin-left: 40px;
      font-size: 15px;
      color: #101a37;
      font-weight: 300;
  }
  .grid-context p{
      padding-top: 20px;
  }
  .index__opportunityTitle {
      margin-top: 42px;
      white-space: pre-wrap!important;
      word-wrap: break-word!important;
      *white-space:normal!important;
      font-size: 38px;
      line-height: 1.5;
      font-weight: 300;
  }
  .index__opportunityResponse1 {
      margin-top: 108px;
  }
  .index__opportunityResponse2 {
      margin-top: 28px;
      margin-bottom: 84px;
  }
  @media screen and (max-width: 770px) {
    .index__opportunityTitle {
        font-size: 20px;
        margin-top: 22px;
        margin-bottom: 0px;
        line-height: 34px;
        font-weight: 300;
        color: black;
    }
    .el-col-xs-12 {
        width: 100%;
    }
    .index__opportunityResponse1 {
        margin-top: 20px;
    }
    .grid-context {
        margin-left: 40px;
    }
  }
</style>
