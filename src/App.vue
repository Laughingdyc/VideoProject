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

    <router-view></router-view>

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
import AppHeader from "@/components/AppHeader"
import AppFooter from "@/components/AppFooter"

export default {
  components: {
    AppHeader,
    AppFooter
  },

}
</script>

<style scoped>
  .el-row {
    margin-bottom: 20px;
  }
  .el-col {
    border-radius: 4px;
  }
</style>