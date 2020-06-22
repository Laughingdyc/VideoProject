<template>
  <div id="Second">
    <el-container>
      <el-aside width="200px">
        <img src="../assets/images/3.png" >
          <div>
            <el-radio-group v-model="radio1">
              <el-radio-button label="数据统计" class="radioGroup"></el-radio-button>
              <el-radio-button label="数据预测" class="radioGroup"></el-radio-button>
              <el-radio-button label="流量分析" class="radioGroup"></el-radio-button>
              <el-radio-button label="广告发布" class="radioGroup"></el-radio-button>
            </el-radio-group>
          </div>
      </el-aside>
      <el-main>
        <sec-main></sec-main>
      </el-main>
    </el-container>
  </div>
</template>

<script>
  import SecMain from "@/components/SecMain";
  export default {
    components: {
      SecMain
    },
    data () {
      return {
        radio1: '流量分析'
      }
    }
  }
</script>


<style scoped>
  .radioGroup{
    width: 200px;
  }
  ul li{
    line-height: 30px;
    text-align: left;
    list-style: none;
  }
  #Second{
    margin: 20px 200px;
  }
  
  .el-aside {
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>