<template>
  <div>
    <h1>流量分析</h1>
    <p>是指在获得网站访问量基本数据的情况下对有关数据进行统计、分析，从中发现用户访问网站的规律，并将这些规律与网络营销策略等相结合，从而发现目前网络营销活动中可能存在的问题，并为进一步修正或重新制定网络营销策略提供依据。当然这样的定义是站在网络营销管理的角度来考虑的</p>
    <el-aside width="200px">
      <ul>
        <li>购买数量</li>
        <li>产品类型</li>
        <li>有效时间</li>
        <li>产品版本</li>
        <li>总价</li>
      </ul>
    </el-aside>
    <el-main>
      <ul>
        <!-- 购买数量 -->
        <li><el-input-number v-model="num" @change="handleChange" :min="1" :max="10" label="购买数量" ></el-input-number></li>
        <!-- 产品类型 -->
        <li>
          <el-select v-model="value">
            <el-option
              v-for="item in options"
              :key="item.value"
              :label="item.label"
              :value="item.value">
            </el-option>
          </el-select>
        </li>
        <!-- 有效时间 -->
        <li>
          <div class="trueYear">   
            <el-radio-group v-model="year">
              <el-radio-button label="半年"></el-radio-button>
              <el-radio-button label="一年"></el-radio-button>
              <el-radio-button label="三年"></el-radio-button>
            </el-radio-group>
          </div>
        </li>
        <!-- 产品版本 -->
        <li>
          <div class="trueYear">   
            <el-radio-group v-model="ed">
              <el-radio-button label="客户版"></el-radio-button>
              <el-radio-button label="代理商版"></el-radio-button>
              <el-radio-button label="专家版"></el-radio-button>
            </el-radio-group>
          </div>
        </li>
        <!-- 总价 -->
        <li>
          <span>998元</span>
        </li>
      </ul>

    </el-main>
      <!-- 网站下面的一大堆文字 -->
    <div class="manyWords">
      <h1>产品说明</h1>
      <p>网站访问统计分析报告的基础数据源于网站流量统计信息，但其价值远高于原始数据资料。专业的网站访问统计分析报告对网络营销的价值，正如专业的财务分析报告对企业经营策略的价值。</p>
      <h1>用户行为指标</h1>
      <p>用户行为指标主要反映用户是如何来到网站的、在网站上停留了多长时间、访问了哪些页面等，主要的统计指标包括：</p>
      <p>用户在网站的停留时间；</p>
      <p>用户来源网站（也叫“引导网站”）；</p>
      <p>用户所使用的搜索引擎及其关键词；</p>
      <p>在不同时段的用户访问量情况等。</p>
      <h1>浏览网站方式</h1>
      <p>用户上网设备类型</p>
      <p>用户浏览器的名称和版本</p>
      <p>访问者电脑分辨率显示模式</p>
      <p>用户所使用的操作系统名称和版本</p>
      <p>用户所在地理区域分布状况等</p>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        num: 1,
        year: '半年',
        ed: '客户版',
        options: [{
          value: '选项1',
          label: '入门'
        }, {
          value: '选项2',
          label: '中级'
        }, {
          value: '选项3',
          label: '高级'
        }],
        value: '选项1'
      };
    },
    methods: {
      handleChange(value) {
        console.log(value);
      }
    }
  };
</script>

<style scoped>
  .manyWords{
    float: left;
    display: inline-block;
  }
  .trueYear{
    float: inline;
    margin: 0;
    padding: 0;
    line-height: 40px;
  }
  .numInput {
    margin: 0;
    padding: 0;
    float: left;
    line-height: 40px;
  }
  .el-main > ul li {
    top: -20px;
    padding: 10px;
    line-height: 40px;
    list-style: none;
    text-align: left;
  }
  .el-aside > ul li{
    padding: 10px;
    line-height: 40px;
    list-style: none;
  }
  h1{
    text-align: left;
    line-height: 50px;
  }
  p{
    line-height: 20px;
    text-align: left;
  }
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    float: left;
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    padding: 0;
  }
  
  .el-main {
    padding: 0;
    float: left;
    width: 600px;
    background-color: #E9EEF3;
    color: #333;
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