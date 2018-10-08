<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        The R-Token Standard, a building block for crypto-securities compliance
                    </div>
                    <div class="header_detail">
                        The Regulated Token (R-Token) is an open source standard and a core component of the Harbor compliance protocol. R-Token applies regulatory compliance at every step and across jurisdictions — from issuance to secondary trades.
                    </div>
                    <div class="header_more_feature">
                        <el-row>
                            <el-col :span="12">
                                <div class="grid-content bg-purple">
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            ERC-20 compatible and works with the existing Ethereum ecosystem
                                        </div>
                                    </div>
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            ERC-20 compatible and works with the existing Ethereum ecosystem
                                        </div>
                                    </div>
                                </div>
                            </el-col>
                            <el-col :span="12">
                                <div class="grid-content bg-purple-light">
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            ERC-20 compatible and works with the existing Ethereum ecosystem
                                        </div>
                                    </div>
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            ERC-20 compatible and works with the existing Ethereum ecosystem
                                        </div>
                                    </div>
                                </div>
                            </el-col>
                        </el-row>
                    </div>
                    <div class="header_feature_content">
                        <div class="index__platformStepDetail">
                            R-Token compliance at a glance
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">1</div>
                                <div class="step__title">Faster, Easier, Low-Cost Capital Formation</div>
                                <div class="step__detail">
                                    <p>
                                        The R-Token embeds rules to ensure only eligible investors can trade the token. Issuers can also limit the number of investors and require holding periods.
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">2</div>
                                <div class="step__title">Faster, Easier, Low-Cost Capital Formation</div>
                                <div class="step__detail">
                                    <p>
                                        The R-Token embeds rules to ensure only eligible investors can trade the token. Issuers can also limit the number of investors and require holding periods.
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">3</div>
                                <div class="step__title">Faster, Easier, Low-Cost Capital Formation</div>
                                <div class="step__detail">
                                    <p>
                                        The R-Token embeds rules to ensure only eligible investors can trade the token. Issuers can also limit the number of investors and require holding periods.
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="header_link_row">
                        <router-link to="#">Broker-Dealers</router-link>
                        <div class="header_link_divide"></div>
                        <router-link to="#">Issuers</router-link>
                        <div class="header_link_divide"></div>
                        <router-link to="#">Parthers</router-link>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderFeatureMore'
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
  .header_more_feature {
    margin: 0 auto;
    margin-top: 43px;
    margin-bottom: 28px;
    height: 168px;
    width: 100%;
    max-width: 932px;
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
  .index__platformStepDetail {
      color: #101a37;
      font-weight: 300;
      text-align: center;
      font-size: 32px;
  }
  .step__stepNumber {
      font-size: 52px;
      font-weight: 600;
      line-height: 60px;
  }
  .step__title {
      margin-top: 14px;
  }
  .step__detail p{
    font-size: 16px;
    margin-top: 12px;
    margin-bottom: 28px;
    color: #727988;
    font-weight: 300;
  }
  .step__center {
      padding-right: 30px;
  }
  .header_link_row {
      margin: 0 auto;
      margin: 32px 0 98px 0;
      text-align: center;
  }
  .header_link_row a {
      color: #0fa5f2;
      text-decoration: none;
  }
  .header_link_row .header_link_divide {
      display: inline-flex;
      width: 2px;
      height: 20px;
      border: 1px solid #d6e7f1;
      box-sizing: border-box;
      background: #bbb;
      margin: 0px 25px;
  }
</style>
