<template>
    <div>
        <el-row>
            <el-col :span="24">
                <div class="grid-content bg-purple">
                    <div class="home_footer">
                        <a href="">© 2018 Harbor Platform, Inc</a>
                        <a href="">Newsroom</a>
                        <a href="">Partnership Inquiries</a>
                        <a href="">Privacy Policy</a>
                    </div>
                </div>
            </el-col>
        </el-row>
    </div>
</template>
<script>
export default {
  name: 'HomeFooterInformation'
}
</script>
<style lang="scss" scoped>
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
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .home_footer {
      text-align: center;
      margin: 40px 0px;
  }
  .home_footer a {
      text-decoration: none;
      margin-right: 40px;
      color: #727988;
      font-weight: 300;
  }
</style>
