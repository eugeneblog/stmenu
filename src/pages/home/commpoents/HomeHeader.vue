<template>
    <div>
      <el-row :gutter="20">
        <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="18">
          <div class="grid-content bg-purple-light">
            <img src="https://harbor.com/images/harbor-logo.svg" alt="logo">
          </div>
          <div class="navbar-right">
            <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal">
              <el-menu-item index="1">产品/服务</el-menu-item>
              <el-menu-item index="2">白⽪书</el-menu-item>
              <el-menu-item index="3">关于我们</el-menu-item>
            </el-menu>
          </div>
        </el-col>
        <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  }
}
</script>

<style lang="scss" scoped>
    .el-row {

    margin-top: 20px;
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
  .bg-purple-light {
    position: absolute;
    top: 50%;
    height: 60px;
    margin-top: -30px;
    float: left;
  }
  .bg-purple-light img{
    height: 34px;
    margin-top: 20px;
    vertical-align: middle;
  }
  .el-menu-demo {
    border-bottom: none;
    float: right;
  }
  .el-menu--horizontal,.el-menu--horizontal>.el-menu-item {
    border-bottom: none;
  }
  .el-menu--horizontal>.el-menu-item.is-active{
    border-bottom: 0px;
  }
  .navbar-right{
    height: 60px;
  }
</style>
