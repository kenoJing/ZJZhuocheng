<script setup lang="ts">
const visionModuleList = [
  {
    image:
      "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAg2vaGqgYomI-wuQcw8AU48AU.png",
    title: "定位",
    text: "立足国内市场，走向世界",
  },
  {
    image:
      "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgm-OGqgYouuTb4wMw8AU48AU.png",
    title: "理念",
    text: "诚信、敬业、务实、创新",
  },
  {
    image:
      "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgm-OGqgYo9tevtwQw8AU48AU.png",
    title: "目标",
    text: "国际化、品牌化、专业化",
  },
  {
    image:
      "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgm-OGqgYonMm9nQMw8AU48AU.png",
    title: "使命",
    text: "成就客户、成就品牌、成就员工",
  },
];
</script>
<template>
  <div>
    <el-image
      class="banner"
      src="https://31728769.s21i.faiusr.com/4/ABUIABAEGAAgle2GqgYojI_ilQYwyA84vgM.png"
    ></el-image>
    <div class="main">
      <el-image
        class="main-left"
        src="
http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgo_2GqgYo8KOMrAcwwQQ4jQM.png.webp"
      ></el-image>
      <div class="main-right">
        <div class="main-right-title">关于我们</div>
        <div class="main-right-subtitle">ABOUT US</div>
        <div class="main-right-content">
          浙江卓成精密机械有限公司成立于2021年4月，地处浙江省衢州市。公司总部位于浙江省杭州市。公司专注于螺杆压缩主机等流体动力核心技术及产品的研发、制造与销售，致力于成为全球领先的流体动力服务商。公司产品在工业自动化、工程掘进、轨道交通及石油化工等领域被广泛使用，在行业内树立了良好的品牌形象和口碑。
        </div>
      </div>
    </div>
    <div class="vision">
      <div class="vision-content">
        <div class="vision-title">
          公司理念
          <div class="vision-subtitle">OUR VISION</div>
        </div>
        <div class="vision-modules">
          <div
            class="vision-module-item"
            v-for="item in visionModuleList"
            :key="item.title"
          >
            <el-image
              :src="item.image"
              class="vision-module-item-image"
            ></el-image>
            <div class="vision-module-item-title">{{ item.title }}</div>
            <div class="vision-module-item-text">{{ item.text }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.banner {
  height: 477px;
}

.main {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 737px;
}

.main .main-left,
.main .main-right {
  width: 720px;
  height: 402px;
  padding: 0 38px;
  max-width: 50%;
}

.main-right-title {
  font-size: 20px;
  color: rgb(51, 51, 51);
  font-family: 微软雅黑;
  text-align: left;
  font-size: 24px;
  font-weight: 700;
}

.main-right-subtitle {
  font-size: 20px;
  color: rgb(51, 51, 51);
  font-family: 微软雅黑;
  text-align: left;
  color: rgb(153, 153, 153);
  font-size: 16px;
}

.main-right-content {
  margin-top: 14.5px;
  color: #333;
  font-family: 微软雅黑;
  font-size: 20px;
  text-align: left;
  line-height: 34px;
}

.vision {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 789px;
  background-image: url("http://31728769.s21i.faiusr.com/2/ABUIABACGAAgwvKHqgYokI7NHzCADzjYBA.jpg.webp");
  background-size: cover;
  font-family: 微软雅黑;
}

.vision-content {
  max-width: 1440px;
}

.vision-title {
  line-height: 36px;
  font-size: 24px;
  color: rgb(51, 51, 51);
  text-align: center;
  font-weight: 700;
}

.vision-subtitle {
  color: rgb(153, 153, 153);
  font-size: 16px;
  height: 30px;
  line-height: 30px;
}

.vision-modules {
  display: flex;
  max-width: 1440px;
  width: 100vw;
  height: 351px;
  margin-top: 33px;
  padding: 14px;
  justify-content: space-between;
}
.vision-module-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 23.5%;
  height: 100%;
  padding: 50px;
  background-color: #fff;
}

.vision-module-item-image {
  height: 133px;
}
.vision-module-item-title {
  margin-top: 30px;
  font-size: 18px;
}
.vision-module-item-text {
  margin-top: 12px;
  font-size: 14px;
  color: rgb(153, 153, 153);
}
</style>