<template>
    <div class="home-main">
        <el-row>
            <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
            <el-col :span="18">
                <div class="grid-content bg-purple-light">
                    <div class="header_title">
                        {{ mainContext.title }}
                    </div>
                    <div class="header_detail">
                        {{ mainContext.detail }}
                    </div>
                    <div class="header_button">
                        <router-link to="about">{{ mainContext.button }}</router-link>
                    </div>
                    <div class="header_link_row">
                        <template v-for="item in mainContext.link" >
                            <div v-if="item.id > 1"
                                class="header_link_divide"
                                :key='item.id+1'
                                ></div>
                            <router-link
                            :to = 'item.href'
                            :key = 'item.id'
                            >
                                {{ item.text }}
                            </router-link>
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
  name: 'HomeMain',
  props: {
    mainContext: Object
  }
}
</script>

<style lang="scss" scoped>
.home-main {
    background: url('/static/img/hero-illustration.svg');
    background-position: 50% -380px;
}
.el-row {
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
    margin: 46px 10px 0px 10px;
    font-size: 48px;
    text-align: center;
    color: #1b1d2e;
    line-height: 64px;
    font-weight: 300;
    text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.3)
  }
  .header_detail {
    font-size: 22px;
    margin: 0 auto;
    color: #3c3e40;
    margin-top: 24px;
    line-height: 38px;
    font-weight: 300;
    text-align: center;
    text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.3);
    overflow: hidden;
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
  @media screen and (max-width: 760px) {
    .header_title{
      font-size: 30px;
      margin-top: 12px;
    }
    .header_detail {
      margin-top: 8px;
      font-size: 12px;
    }
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
  }
</style>
