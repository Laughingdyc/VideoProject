<template>
  <div id="app">
    <!-- header -->
    <el-row>
      <el-col :span="24">
        <div>
          <app-header></app-header>
        </div>
      </el-col>
    </el-row>

    <!-- main -->
    <el-row>
      <!-- 左边留白 -->
      <el-col :span="3"><div class="grid-content bg-white"></div></el-col>
      <!-- 左边菜单栏 -->
      <el-col :span="4">
        <div class="grid-content bg-white">
          <main-left-up></main-left-up>
          <!-- 菜单栏中间的留白 -->
          <div class="block-10px"></div>
          <main-left-down></main-left-down>
        </div>
      </el-col>
      <!-- 主体区, 包括图片滚动和四个小模块 -->
      <el-col :span="14"><div class="grid-content bg-purple"></div></el-col>
      <!-- 右边留白 -->
      <el-col :span="3"><div class="grid-content bg-white"></div></el-col>
    </el-row>

    <!-- footer -->
    <el-row>
      <el-col :span="24">
        <div>
          <app-footer></app-footer>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import MainLeftUp from '@/components/mainComponents/MainLeftUp'
import MainLeftDown from '@/components/mainComponents/MainLeftDown'
import AppHeader from '@/components/AppHeader'
import AppFooter from '@/components/AppFooter'

export default {
  components: {
    AppHeader,
    MainLeftUp,
    MainLeftDown,
    AppFooter
  }
}
</script>

<style scoped>
  .block-10px{
    height: 10px;
  }
  .el-row {
    margin-bottom: 20px;
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-white{
    background: white;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>