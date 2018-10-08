<template>
    <div class="header_description">
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content">
                    <div class="header_des_title">
                        <div class="index__opportunityDots">
                            <img src="https://harbor.com/images/index/opportunity/blockchain-three-dots.svg" alt="">
                        </div>
                        <div class="index__opportunityTitle">
                            Lock up capital, <br/>
                            not investors.
                        </div>
                    </div>
                    <div class="header_des_content">
                        <p>Tokenization is the process of converting rights to an asset into a digital token on a blockchain. Blockchains can transform private securities by making capital formation faster, easier, and less expensive while unlocking secondary liquidity (and value) for investors.</p>
                        <p>The Harbor platform and compliance protocol ensure tokenized securities comply with existing securities laws at issuance and on every trade, everywhere across the globe.</p>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderMainDescription'
}
</script>

<style lang="scss" scoped>
  .header_descrioption{
      background: #f6f6f6;
  }
  .el-row {
    background: #f6f6f6;
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
    height: 372px;
    overflow: hidden;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .header_des_title {
      display: block;
      float: left;
  }
  .header_des_content {
      display: block;
      width: 800px;
      float: right;
      color: #474b59;
  }
  .header_des_content p:first-child{
      margin-top: 108px;
      font-size: 16px;
      color: #474b59;
      font-weight: 300;
  }
  .header_des_content p:last-child {
      font-size: 16px;
      margin-top: 28px;
      margin-bottom: 84px!important;
      color: #474b59;
      font-weight: 300;
  }
  .index__opportunityDots {
      margin-top: 59px;
  }
  .index__opportunityTitle {
      margin-top: 47px;
      font-size: 40px;
      font-weight: 300;
  }
</style>
