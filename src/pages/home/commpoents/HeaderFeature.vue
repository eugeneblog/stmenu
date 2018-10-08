<template>
    <div>
        <el-row>
            <!-- <div class="rowContainer_backgroundContent">
                <img class="index__leftSlashes" src="https://harbor.com/images/index/mobile/blue_on_white_stripes.svg" alt="">
            </div> -->
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        欢迎进⼊资产数字化时代
                    </div>
                    <div class="header_detail">
                        TOKEN化改变了传统资产的形态，提⾼二级交易的动态，为发行人和经纪商创造令新的市场机会，以新的⽅方式颗粒化资产，并吸引全球投资者。
                    </div>
                    <div class="header_feature_content">
                        <div class="header_feature_item">
                            <div>更快、更容易、低成本的资产形成</div>
                            <ul>
                                <li>对单个资产进行TOKEN化</li>
                                <li>通过技术实施合规管理</li>
                                <li>保持准确的记录</li>
                            </ul>
                        </div>
                        <div class="header_feature_item">
                            <div>促进资金流动</div>
                            <ul>
                                <li>促进快速结算</li>
                                <li>改善流动性和价值</li>
                                <li>实施⼆级交易合规</li>
                            </ul>
                        </div>
                        <div class="header_feature_item">
                            <div>吸引新投资者</div>
                            <ul>
                                <li>通过分拆来降低投资最低额度</li>
                                <li>通过重新捆绑创建新的基金类型</li>
                                <li>覆盖全球投资者</li>
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
  name: 'HeaderFeature'
}
</script>

<style lang="scss" scoped>
.el-row {
    background: #eaf6fb;
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
    width: 770px;
    max-width: 980px;
    margin: 0 auto;
    color: #727988;
    margin-top: 16px;
    font-weight: 300;
    text-align: center;
    line-height: 1.75;
  }
  .header_feature_content {
      margin: 0 auto;
      height: 256px;
      margin: 32px 0 60px 0;
      text-align: center;
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
</style>
