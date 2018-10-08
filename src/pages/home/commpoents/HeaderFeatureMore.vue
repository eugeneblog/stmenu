<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        S-Token标准加密资产合规的基石
                    </div>
                    <div class="header_detail">
                        S-Token是一个开源标准，是Stmenu Compliance协议的核⼼部分。S-Token在每个步骤和跨辖区(从发行到交易)都符合法规。
                    </div>
                    <div class="header_more_feature">
                        <el-row>
                            <el-col :span="12">
                                <div class="grid-content bg-purple">
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            ERC-1400兼容并与现有的以太坊⽣态系统协同⼯作
                                        </div>
                                    </div>
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            转帐只能在满⾜交易条件的白名单之间进行
                                        </div>
                                    </div>
                                </div>
                            </el-col>
                            <el-col :span="12">
                                <div class="grid-content bg-purple-light">
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            灵活的框架，以执行证券法规、KYC / AML政策、税收规则等。
                                        </div>
                                    </div>
                                    <div class="header_more_feature_item__content">
                                        <i class="el-icon-check"></i>
                                        <div class="header_more_feature_item__text">
                                            在token级别跨交易平台遵从各国家/区域合规性
                                        </div>
                                    </div>
                                </div>
                            </el-col>
                        </el-row>
                    </div>
                    <div class="header_feature_content">
                        <div class="index__platformStepDetail">
                            S-Token合规性⼀目了然
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">1</div>
                                <div class="step__title">S-Tokens将合规性转化为代码</div>
                                <div class="step__detail">
                                    <p>
                                        S-Token嵌入规则以确保只有符合条件的投资者可以交易token，发行人也可以限制投资者的数量并设定持有期限。
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">2</div>
                                <div class="step__title">潜在投资者必须得到验证。</div>
                                <div class="step__detail">
                                    <p>
                                        投资者通过验证流程(KYC / AML / Accreditation)来确定token持有者资格。认可的投资者被添加到以太坊区块链的白名单中。
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="header_feature_item">
                            <div class="step__center">
                                <div class="step__stepNumber">3</div>
                                <div class="step__title">S-Token⾃我管理所有交易。</div>
                                <div class="step__detail">
                                    <p>
                                        启动交易时，S-Token会检查白名单以确认符合法规要求。如果是，则交易被批准。
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="header_link_row">
                        <router-link to="#">阅读白皮书</router-link>
                        <div class="header_link_divide"></div>
                        <router-link to="#">访问github</router-link>
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
