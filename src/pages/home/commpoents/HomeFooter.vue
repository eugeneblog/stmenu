<template>
    <div>
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        <img :src="context.logoUrl" alt="">
                    </div>
                    <div class="header_detail">
                       {{ context.title }}
                    </div>
                    <div class="header_button">
                        <router-link to="whitePaper">{{ context.button }}</router-link>
                    </div>
                </div>
            </el-col>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HomeFooter',
  data () {
    return {
      context: {
        logoUrl: require('../../../assets/img/footerLogo@3x.png'),
        title: '查看stmenu白皮书',
        button: '点击查看'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.el-row {
    background: -webkit-gradient(linear,left top,left bottom,from(#9dc0b9),to(#63808b));
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
    color: #ffffff;
    line-height: 64px;
    font-weight: 300;
  }
  .header_detail {
    font-size: 32px;
    margin: 0 auto;
    color: #ffffff;
    margin-top: 24px;
    line-height: 44px;
    font-weight: 300;
    text-align: center;
  }
  .header_button {
      margin-top: 40px;
      font-weight: 400;
      margin-bottom: 60px;
      text-align: center;
  }
  .header_button > a{
      background: #25419a;
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
      background: #2447b0;
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
  .header_title > img {
        width: 56px;
        height: 56px;
  }
  @media screen and (max-width: 760px) {
    .header_title {
        margin: 34px 10px 0px 10px;
    }
    .header_title > img {
        width: 48px;
        height: 48px;
    }
    .header_detail {
        font-size: 24px;
        margin-top: 24px;
        line-height: 24px;
    }
    .header_button > a{
      width: 300px;
      height: 48px;
      line-height: 48px;
      font-size: 18px;
    }
  }
</style>
