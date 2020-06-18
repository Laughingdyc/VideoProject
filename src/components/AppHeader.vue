<template>
  <div id="header">
    <!-- 左边的logo图片 -->
    <img src="../assets/logo.png" alt="VueLogo" id="logo">

    <!-- 右边的三个链接 -->
    <div class="link-span">
      <span>登录</span> |
      <span>注册</span> |
      <span>关于</span>
    </div>
  </div>
</template>

<style scoped>
  #logo{
    position: relative;
    width: 100px;
    left: 10%;
  }
  #header{
    background-color: #d0d0d0;
  }
  .link-span{
    position: relative;
    float: right;
    font-size: 14px;
    line-height: 100px;
    right: 10%;
  }
</style>