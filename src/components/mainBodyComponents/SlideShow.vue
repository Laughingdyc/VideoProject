<template>
  <div id="slideShow">
    <div class="block">
      <el-carousel  type='card' height="280px">
        <el-carousel-item v-for="(img, index) in slidePicSrc" :key="index">
          <img :src="img.url" @click="gotoSecond">
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  props: ['slidePicSrc'],
  methods: {
    gotoSecond () {
      this.$router.push('/second')
    }
  }

}
</script>

<style scoped>
  img{
    height: 280px;
  }
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
     background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
     background-color: #d3dce6;
  }
</style>