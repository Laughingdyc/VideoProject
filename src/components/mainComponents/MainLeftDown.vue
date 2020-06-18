<template>
  <div id="mainLeftUp">
    <el-container>
      <!-- 标题 -->
      <el-header height="30px" class="bg-black">
        最新消息
      </el-header>

      <!-- 主体的内容 -->
      <el-main class="bg-pink">
        <ul>
          <li v-for="item of Items" :key="item">
            {{ item }}
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
      Items: [
        '新闻条目1',
        '新闻条目2',
        '新闻条目3',
        '新闻条目4'
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
  .bg-black{
    background: #4a4a4a;
  }
  .bg-pink{
    background: pink;
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