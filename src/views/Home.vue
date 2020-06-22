<template>
  <div>
    <div>
      <!-- main -->
      <el-container>
        <!-- 左边菜单栏 -->
        <el-aside width="200px">
          <main-left-up></main-left-up>
          <!-- 菜单栏中间的留白 -->
          <div class="block-10px"></div>
          <main-left-down></main-left-down>
          <div class="footBlock"></div>
        </el-aside>

        <!-- 主体区 -->
        <el-main >
          <div id="mainDiv">
            <!-- 图片滚动 -->
            <slide-show :slidePicSrc='picSrc'></slide-show>

            <!-- 四个小组件 -->
            <div class="mainFourDiv">
              <div v-for="(img, index) in imageSrc" :key="index">
                <main-link-component 
                :mainLinkPicSrc='img.url'
                :contentHeader='img.headerContent'
                :contentBody='img.bodyContent'></main-link-component>
              </div>
            </div>
          </div>
        </el-main>
      </el-container>
    </div>
  </div>
</template>

<script>

import MainLeftUp from "@/components/mainLeftComponents/MainLeftDown"
import MainLeftDown from "@/components/mainLeftComponents/MainLeftUp"
import MainLinkComponent from "@/components/mainBodyComponents/MainLinkComponent"
import SlideShow from "@/components/mainBodyComponents/SlideShow"

export default {
  components: {
    MainLeftUp,
    MainLeftDown,
    SlideShow,
    MainLinkComponent
  },
  data () {
    return {
      picSrc: [
        {url: require('@/assets/slideShow/pic1.jpg')},
        {url: require('@/assets/slideShow/pic2.jpg')},
        {url: require('@/assets/slideShow/pic3.jpg')},
        {url: require('@/assets/slideShow/pic4.jpg')}
      ],
      imageSrc: [
        {
          url: require('@/assets/images/1.png'),
          headerContent: '开放产品',
          bodyContent: '开放产品时一款开放产品'
        },
        {
          url: require('@/assets/images/2.png'),
          headerContent: '品牌营销',
          bodyContent: '品牌营销帮助你的产品更好地找到定位'
        },{
          url: require('@/assets/images/3.png'),
          headerContent: '使命必达',
          bodyContent: '使命必达快速迭代永远保持最前端的速度'
        },{
          url: require('@/assets/images/4.png'),
          headerContent: '勇攀高峰',
          bodyContent: '帮你勇闯高峰，到达事业的顶峰'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .footBlock{
    height: 200px;
  }
  .mainFourDiv > div{
    float: left;
    width: 500px;
  }
  #mainDiv{
    width: 1000px;
  }
  .block-10px{
    height: 10px;
  }


  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    margin-left: 10%;
  }
  
  .el-main {
    padding: 0;
    margin-left: 20px;
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
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