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
                        Welcome to the digital age of private securities
                    </div>
                    <div class="header_detail">
Tokenization changes the economics of capital formation and the dynamics of secondary trading. It creates exciting new opportunities for issuers and broker-dealers to unbundle and bundle assets in new ways and reach investors globally.
                    </div>
                </div>
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        Welcome to the digital age of private securities
                    </div>
                    <div class="header_detail">
Tokenization changes the economics of capital formation and the dynamics of secondary trading. It creates exciting new opportunities for issuers and broker-dealers to unbundle and bundle assets in new ways and reach investors globally.
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HomeExample'
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
</style>
