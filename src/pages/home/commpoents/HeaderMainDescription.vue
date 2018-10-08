<template>
    <div>
        <el-row>
            <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="8">
                <div class="grid-content bg-purple-light">
                    <div class="grid-content-box">
                        <div class="index__opportunityDots">
                            <img src="https://harbor.com/images/index/opportunity/blockchain-three-dots.svg" alt="">
                        </div>
                        <div class="index__opportunityTitle">
                            变更财产观念，<br/>
                            资产数字化是未来趋势。
                        </div>
                    </div>
                </div>
            </el-col>
            <el-col :span="8">
                <div class="grid-content bg-purple-light">
                    <div class="grid-context">
                        <p class="index__opportunityResponse1">资产TOKEN化是将资产权益转换为区块链上token的过程，从而使资本形成更快，更容易和更方便转变为颗粒化财产形态，同时为投资者释放二级流动性和价值</p>
                        <p class="index__opportunityResponse2">Stmenu平台和合规协议确保令牌化证券符合发行时的现有证券法以及全球各地的每笔交易。</p>
                    </div>
                </div>
            </el-col>
            <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderMainDescription'
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
    margin-left: 40px;
  }
  .index__opportunityDots {
      margin-top: 59px;
  }
  .grid-context {
      font-size: 15px;
      color: #101a37;
      font-weight: 300;
  }
  .index__opportunityTitle {
      margin-top: 47px;
      font-size: 40px;
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
</style>
