<template>
  <div id="mainLink">
    <div class="img">
      <img :src="mainLinkPicSrc">
    </div>
    <div class="content">
      <ul>
        <li><p><strong>{{ contentHeader }}</strong></p></li>
        <li><p>{{ contentBody }}</p></li>
        <li><el-button type="success" @click="goToSecond">立即购买</el-button></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'mainLinkPicSrc',
    'contentHeader',
    'contentBody'
  ],
  methods: {  
    goToSecond () {
      this.$router.push('/second')
    }
  }
}
</script>

<style scoped>
  #mainLink{
    margin: 0;
    padding: 0;
  }
  img{
    padding: 20px 0 20px 20px;
    float: left;
    height: 100px;
  }
  .content{
    padding: 0;
    float: left;
    height: 100px;
  }
  ul li{
    text-align: left;
    left: 0;
    list-style: none;
  }

</style>