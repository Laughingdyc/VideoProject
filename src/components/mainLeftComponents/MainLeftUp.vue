<template>
  <div id="mainLeftUp">
    <el-container>
      <!-- 标题 -->
      <el-header height="30px" class="bg-black">
        全部产品
      </el-header>

      <!-- 主体上面的内容 -->
      <el-main class="bg-pink">
        <!-- 上方的列表说明 -->
        <div class="information">
          <span class="font-bold">PC产品</span>
        </div>

        <!-- 下方的列表链接 -->
        <ul>
          <li v-for="item of TopItems" :key="item">
            <router-link :to="{path: '/second'}">{{ item }}</router-link>
          </li>
        </ul>
      </el-main>

      <!-- 主体下面的内容 -->
      <el-main class="bg-pink">
        <!-- 上方的列表说明 -->
        <div class="information">
          <span class="font-bold">手机应用类</span>
        </div>

        <!-- 下方的列表链接 -->
        <ul>
          <li v-for="item of BottomItems" :key="item">
            <router-link :to="{path: '/second'}">{{ item }}</router-link>
          </li>
        </ul>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      TopItems: [
        '数据统计',
        '数据预测',
        '流量分析',
        '广告发布'
      ],
      BottomItems: [
        '91助手',
        '产品助手',
        '智能地图',
        '团队语音'
      ]
    }
  }
}
</script>

<style scoped>
  ul,li{ 
    padding:0;
    margin:0 0 5px 0;
    position: relative;
    left: 7px;
    list-style:none;
    font-size: 14px;
  }
  .information{
    padding-bottom: 20px;
  }
  .bg-black{
    background: #4a4a4a;
  }
  .bg-pink{
    background: pink;
  }
  .font-bold{
    font-size: 14px;
    font-weight: 700;
  }
  .el-header{
    font-size: 14px;
    line-height: 30px;
    color: white;
  }
  .el-main{
    box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1)
  }
</style>