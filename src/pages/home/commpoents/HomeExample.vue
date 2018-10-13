<template>
    <div>
        <el-row>
            <el-col  :xs="1" :sm="3" :md="3" :xl="9" :lg="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col  :xs="22" :sm="18" :md="18" :xl="9" :lg="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        {{ context.title }}
                    </div>
                </div>
            </el-col>
            <el-col  :xs="1" :sm="3" :md="39" :xl="9" :lg="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
        <el-row>
            <el-col :xs="0" :sm="3" :md="3" :xl="3" :lg="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :xs="12" :sm="9" :md="9" :xl="9" :lg="9">
                <div class="grid-content bg-purple-light">
                    <div class="home_example_context">
                        <p
                        v-for="item in context.texts"
                        :key="item.id"
                        >
                            {{ item.text }}
                        </p>
                    </div>
                </div>
            </el-col>
            <el-col :xs="12" :sm="10" :md="9" :xl="9" :lg="9">
                <div class="home_example_backgroundImg">
                    <div class="home_exaple_imgBox">
                        <img :src='context.backgroundImg' alt="">
                    </div>
                </div>
            </el-col>
            <el-col :xs="0" :sm="2" :md="3" :xl="3" :lg="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HomeExample',
  data () {
    return {
      context: {
        title: '现实世界的例子:房地产',
        texts: [
          {
            id: 1,
            text: '包括房地产基金、房地产投资信托基金、房屋所有权在内的资产可以借助区块链技术提⾼流转效率、透明度获得收益。Stmenu的合规协议和平台解决了复杂的法律、税务和合同要求。'
          }, {
            id: 2,
            text: '我们的使命通过建立分散的合规协议支持加密资产，该协议规范了了加密资产在区块链上的发行和交易。'
          }
        ],
        backgroundImg: 'https://harbor.com/images/index/buildings.svg'
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
  .index__leftSlashes{
    position: absolute;
    left: 0;
    bottom: 0;
  }
  .header_title {
    margin-top: 87px;
    width: 100%;
    font-size: 32px;
    text-align: left;
    color: #1b1d2e;
    line-height: 64px;
    font-weight: 300;
  }
  .home_example_context {
      margin-top: 24px;
      padding-left: 10px;
      margin-bottom: 140px;
  }
  .home_example_context p:last-child {
      margin-top: 24px;
  }
  .home_example_context p {
      font-size: 14px;
      line-height: 26px;
      font-weight: 300;
  }
  .home_example_backgroundImg {
      margin-left: 100px;
      margin-top: 80px;
  }
  .home_exaple_imgBox > img{
      display: block;
      background-size: 100%;
      width: 100%;
      height: 100%;
  }
  @media screen and (max-width: 768px) {
      .el-col-xs-12 {
          width: 100%;
      }
      .home_exaple_imgBox > img{
        position: absolute;
        width: 288px;
        height: 135px;
        right: 5%;
        bottom: 38px;
      }
      .header_title {
          font-size: 24px;
      }
  }
</style>
