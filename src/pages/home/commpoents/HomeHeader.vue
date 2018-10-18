<template>
    <div>
      <el-row :gutter="20">
        <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="18">
          <div class="grid-content bg-purple-light">
            <img :src = 'headerList.logoUrl' alt="logo">
          </div>
          <div
          class="navbar-right"
          :class="{ isHidden : isMobile }"
          v-show="!isMobile"
          >
            <el-menu
            :default-active="activeIndex"
            class="el-menu-demo"
            mode="horizontal">
              <router-link
              v-for="item of headerList.title"
              :key='item.index'
              :to = "item.link"
              class="header-link-a"
              >
                <el-menu-item
                :index="String(item.index)"
                >
                  {{ item.text }}
                </el-menu-item>
              </router-link>
            </el-menu>
          </div>
          <div v-show="isMobile" class="mobile-navbar">
            <span class="mobile-navbar-menu" @click="isShowHandleClick">菜单</span>
            <div class="mobild-navbar-list" v-show="isShowMobScreen">
              <div class="mobild-navbar-close">
                <i class="el-icon-close" @click="isShowHandleClick"></i>
              </div>
              <ul>
                <li
                v-for="item of headerList.title"
                :key = 'item.index'
                >
                  <router-link :to="item.link">{{ item.text }}</router-link>
                </li>
              </ul>
            </div>
          </div>
        </el-col>
        <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    headerList: Object
  },
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      isMobile: false,
      isShowMobScreen: false
    }
  },
  created () {
    this.changeMediaScreen(this)
  },
  mounted () {
    const _this = this
    window.onresize = () => {
      _this.changeMediaScreen(_this)
    }
  },
  methods: {
    getScreenWidth () {
      return window.outerWidth
    },
    changeMediaScreen (el) {
      let winWidth = this.getScreenWidth()
      if (winWidth >= 760) {
        el.isMobile = false
      } else {
        el.isMobile = true
      }
    },
    isShowHandleClick () {
      this.isShowMobScreen = !this.isShowMobScreen
    }
  }
}
</script>

<style lang="scss" scoped>
  .header-link-a{
    float: left;
    text-decoration: none;
  }
  .el-row {
      margin-top: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
 .grid-content {
  min-height: 36px;
}
.bg-purple-light {
  position: absolute;
  top: 50%;
  margin-top: -30px;
  float: left;
  img {
    height: 34px;
    margin-top: 20px;
    vertical-align: middle;
  }
}
.el-menu-demo {
  border-bottom: none;
  float: right;
}
.el-menu--horizontal,.el-menu--horizontal>.el-menu-item {
  border-bottom: none;
}
.el-menu--horizontal {
  & > .el-menu-item {
    &.is-active {
      border-bottom: 0px;
    }
  }
}
.isHidden {
  display: none;
}
.mobile-navbar {
  float: right;
  color: #464b5a;
  font-weight: 300;
}
.mobild-navbar-list {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background: #3c4253;
  z-index: 999;
  a {
    display: block;
    margin-top: 48px;
    text-decoration: none;
    color: #dadce4;
    &:hover {
      text-decoration: underline;
      font-weight: 400;
    }
  }
  ul {
    margin: 0;
    padding: 8px 40px 68px 40px;
  }
}
.mobild-navbar-close {
  margin-right: 10px;
  width: 50px;
  float: right;
  font-size: 34px;
  font-weight: 300;
  color: #dadcda;
  text-align: right;
  i {
    padding: 15px;
    &:hover {
      cursor: pointer;
      font-weight: 400;
    }
  }
}
.mobile-navbar-menu {
  cursor: pointer;
}
@media screen and (max-width: 760px) {
  .bg-purple-light img{
    height: 20px;
  }
}
</style>
