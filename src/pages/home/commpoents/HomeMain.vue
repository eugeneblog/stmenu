<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        Reengineering Private Securities with Blockchains
                    </div>
                    <div class="header_detail">
                        Harbor is the compliance platform for tokenizing private securities such as real estate, company equity, investment funds, fine art, etc.
                    </div>
                    <div class="header_button">
                        <router-link to="about">Contact Us</router-link>
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
  name: 'HomeMain'
}
</script>

<style lang="scss" scoped>
.el-row {
    height: 470px;
    margin-top: 20px;
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
  .rowContainer_backgroundContent {
    height: 470px;
    position: relative;
  }
  .index__leftSlashes{
    position: absolute;
    left: 0;
    bottom: 0;
    width: 275px;
    height: 328px;
  }
  .header_title {
    margin: 56px 10px 0px 10px;
    width: 100%;
    font-size: 48px;
    text-align: center;
    color: #1b1d2e;
    line-height: 64px;
    font-weight: 300;
  }
  .header_detail {
    font-size: 22px;
    width: 770px;
    margin: 0 auto;
    color: #727988;
    margin-top: 24px;
    line-height: 38px;
    font-weight: 300;
    text-align: center;
  }
  .header_button {
      margin-top: 40px;
      text-align: center;
  }
  .header_button > a{
      background: #121a35;
      color: #fff;
      margin: 0 auto;
      display: block;
      width: 227px;
      height: 56px;
      line-height: 56px;
      text-decoration: none;
      font-size: 18px;
      border-radius: 5px;
  }
  .header_button > a:hover {
      background: #0b1021;
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
