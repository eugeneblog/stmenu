<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple">
                    <div class="index__platformStepDetail">
                            {{ context.title }}
                    </div>
                    <div class="header_feature_content">
                        <div
                        class="header_feature_item"
                        v-for="item in context.feature"
                        :key="item.id"
                        >
                            <div class="step__center">
                                <div class="step__stepNumber">{{ item.id }}</div>
                                <div class="step__title">{{ item.title }}</div>
                                <div class="step__detail">
                                    <p>{{ item.text }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="header_link_row">
                        <template v-for="item of context.link">
                            <div v-if="item.id > 1" :key="item.id+1" class="header_link_divide"></div>
                            <router-link :key="item.id" to="#">{{ item.text }}</router-link>
                        </template>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>
<script>
export default {
  name: 'HeaderFeatureDes',
  data () {
    return {
      context: {
        title: 'S-Token合规性⼀目了然',
        feature: [
          {
            id: 1,
            title: 'S-Tokens将合规性转化为代码',
            text: 'S-Token嵌入规则以确保只有符合条件的投资者可以交易token，发行人也可以限制投资者的数量并设定持有期限。'
          }, {
            id: 2,
            title: '潜在投资者必须得到验证。',
            text: '投资者通过验证流程(KYC / AML / Accreditation)来确定token持有者资格。认可的投资者被添加到以太坊区块链的白名单中。'
          }, {
            id: 3,
            title: 'S-Token⾃我管理所有交易。',
            text: '启动交易时，S-Token会检查白名单以确认符合法规要求。如果是，则交易被批准。'
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.el-row {
    background: #ffffff;
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
  .header_feature_content {
      display: flex;
      justify-content: center;
      flex-direction: row;
      align-items: center;
      flex-wrap: wrap;
      margin: 32px 0 60px 0;
  }
  .header_feature_content .header_feature_item {
      margin-top: 40px;
      width:33.33%;
      text-align: left;
      float: left;
  }
  .header_link_row {
      display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        width: 100%;
        flex-direction: row;
        margin-top: 32px;
        margin-bottom: 98px;
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
  @media screen and (max-width: 760px) {
    .header_link_row {
        flex-direction: column;
        margin-top: 32px;
        margin-bottom: 98px;
    }
    .header_link_divide {
        opacity: 0;
    }
    .header_button > a {
        width: 300px;
        height: 48px;
        font-size: 15px;
        line-height: 48px;
    }
    .header_feature_content {
        flex-direction: column;
    }
    .header_feature_content .header_feature_item {
        width: 100%;
    }
    .step__stepNumber {
        font-size: 38px;
        line-height: 38px;
     }
  }
</style>
