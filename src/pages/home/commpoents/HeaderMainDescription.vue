<template>
    <div>
        <el-row :gutter="20">
            <el-col :xs="0" :sm="1" :md="1" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
            <el-col :xs="12" :sm="11" :md="11" :lg="6" :xl="11">
                <div class="grid-content bg-purple-light">
                    <div class="grid-content-box">
                        <div class="index__opportunityDots">
                            <img :src="mainDescription.imgUrl">
                        </div>
                        <pre class="index__opportunityTitle" >{{ mainDescription.title }}</pre>
                    </div>
                </div>
            </el-col>
            <el-col :xs="12" :sm="11" :md="11" :lg="10" :xl="11">
                <div class="grid-content">
                    <div class="grid-context">
                        <p
                        v-for="item in mainDescription.detail"
                        :key="item.id"
                        :class="item.class">{{ item.text }}</p>
                    </div>
                </div>
            </el-col>
            <el-col :xs="0" :sm="1" :md="1" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  name: 'HeaderMainDescription',
  props: {
    mainDescription: Object
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
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .grid-content-box {
      overflow: hidden;
      word-wrap: break-word;
    margin-left: 40px;
  }
  .index__opportunityDots {
      margin-top: 59px;
  }
  .grid-context {
      margin-left: 40px;
      font-size: 15px;
      color: #101a37;
      font-weight: 300;
  }
  .grid-context p{
      padding-top: 20px;
  }
  .index__opportunityTitle {
      margin-top: 42px;
      white-space: pre-wrap!important;
      word-wrap: break-word!important;
      *white-space:normal!important;
      font-size: 38px;
      line-height: 1.5;
      font-weight: 300;
  }
  .index__opportunityResponse1 {
      margin-top: 108px;
  }
  .index__opportunityResponse2 {
      margin-top: 28px;
      margin-bottom: 84px;
  }
  @media screen and (max-width: 770px) {
    .index__opportunityTitle {
        font-size: 20px;
        margin-top: 22px;
        margin-bottom: 0px;
        line-height: 34px;
        font-weight: 300;
        color: black;
    }
    .el-col-xs-12 {
        width: 100%;
    }
    .index__opportunityResponse1 {
        margin-top: 20px;
    }
    .grid-context {
        margin-left: 40px;
    }
  }
</style>
