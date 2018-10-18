<template>
    <div class="about_box">
      <el-container>
        <el-main>
          <img src="../../assets/img/qrcode_for_gh_85e4f6b0af5b_344.jpg" alt="">
        </el-main>
      </el-container>
    </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style lang="scss" scoped>
  body,html {
    height: 100% !important;
    padding: 0px !important;
    margin: 0px !important;
    background: black;
  }
  .about_box {
    background: black;
    height: 100%;
  }
  .el-main {
    // margin: 0 auto;
  }
  .el-main > img {
    display: block;
    margin: 0 auto;
  }
</style>
