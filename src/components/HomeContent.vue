<script setup lang="ts">
import DocumentationIcon from "./icons/IconDocumentation.vue";
import ToolingIcon from "./icons/IconTooling.vue";
import EcosystemIcon from "./icons/IconEcosystem.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";

const bannerImgs = [
  'http://www.jiuyihz.cn/cn/upfiles/201805766224914.jpg',
];

const moduleList = [
  {
    title: '压缩模块',
    img: 'http://www.jiuyihz.cn/cn/upfiles/201805836871157.jpg',
    des: '喷油和无油空压机...',
    link: '/category/integrated-compression',
  },
  {
    title: '精密加工',
    img: 'http://www.jiuyihz.cn/cn/upfiles/201805071757131.jpg',
    des: '转子，外壳，压缩机配件...',
    link: '/category/precision-machining',
  },
  {
    title: '客户定制',
    img: 'http://www.jiuyihz.cn/cn/upfiles/201808151966911.jpg',
    des: '您提要求，我们来设计; 我们是您的私人压缩专家和设计团队...',
    link: '/category/customize-solution',
  }
]

function learnMore() {
 window.open('/production', '_self')
};

</script>

<template>
  <div class="wrapper">
    <div class="header">
      <el-carousel trigger="click" height="100%" v-if="bannerImgs.length > 1">
        <el-carousel-item v-for="item in bannerImgs" :key="item">
          <el-image style="width: 100%; height: 100%" :src="item" fit="cover" loading="lazy" />
        </el-carousel-item>
      </el-carousel>
      <el-image style="width: 100%; height: 100%" :src="bannerImgs[0]" fit="cover" v-if="bannerImgs.length === 1" loading="lazy" />
      <div class="herder-content">
        <div class="herder-content-title">成为全球领先的流体动力服务商</div>
        <el-button round size="large" @click="learnMore">了解更多</el-button>
      </div>
    </div>

    <div class="main">
      <div class="mudules">
        <div class="module-item" v-for="item in moduleList" :key="item.img">
          <a :href="item.link">
            <el-image style="width: 100%; height: 198px" :src="item.img" fit="cover" loading="lazy"/>
          </a>
          <h4 class="module-item-title">
            <a :href="item.link">{{item.title}}</a>
          </h4>
          <div class="module-item-desc">
            <a :href="item.link">{{item.des}}</a>
          </div>
          <div class="module-item-bottom">
            了解更多
          </div>
        </div>
      </div>
    </div>

    <div class="solutions">
      <div class="solutions-title">
        解决方案
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  overflow-y: auto;
}

.header {
  height: 314px;
  width: 100vw;
  position: relative;
}

.herder-content {
  position: absolute;
  left: 31px;
  top: 47px;
  color: #fff;
  font-size: 42px;
  font-family: 'OpenSans','Microsoft YaHei',"微软雅黑",Arial,sans-serif;
}

.herder-content-title {
  line-height: 60px;
  padding: 10px 0 15px 0;
  margin-bottom: 10px;
}

.main {
  padding-top: 10px;
  width: 100vw;
}

.mudules {
  padding: 30px 29px;
  box-sizing: content-box;
  width: calc(100vw - 60px);
  display: flex;
}

.module-item {
  padding: 0 15px;
  width: 33.333%;
  height: 385px;
}

.module-item-title, .module-item-desc {
  text-align: center;
}

.module-item-title {
  margin-top: 10px;
  line-height: 40px;
  font-size: 21px;
  font-weight: 500;
}

.module-item-desc {
  font-size: 16px;
  line-height: 24px;
  height: 72px;
}

.module-item-bottom {
  margin: 20px 0;
  height: 24.5px;
  display: flex;
  justify-content: center;
}

.module-item a {
  text-decoration: none; 
  color: rgb(48, 49, 51);
}

.module-item-desc a:hover{
  color: rgb(64, 158, 255);
}

.solutions {
  padding: 30px 0;
  width: 100vw;
}

.solutions-title {
  text-align: center;
  margin-bottom: 30px;
  line-height: 35px;
  font-weight: 700;
  font-size: 32px;
}
</style>
