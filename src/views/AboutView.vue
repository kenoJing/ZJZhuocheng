
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
    <div class="partners">
      <div class="partners-content">
        合作伙伴
        <div class="partners-content-item">PARTNERS</div>
        <ul class="partners-content-carousel">
          <li
            class="partners-content-carousel-item"
            v-for="item in imageList"
            :key="item.keys"
          >
            <el-image
              :src="item.url"
              class="partners-content-carousel-image"
            ></el-image>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visionModuleList: [
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
      ],
      imageList: [
        {
          keys: 1,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgjeCGqgYoqJuRhQIw4wI4wQE.png.webp",
        },
        {
          keys: 2,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgjOCGqgYow_LfkgQwgQI4qwE.png.webp",
        },
        {
          keys: 3,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgjeCGqgYo8-_0iQIw-QI4wAE.png.webp",
        },
        {
          keys: 4,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgjOCGqgYo5r-_gQIwxAE4RA.png.webp",
        },
        {
          keys: 5,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgjeCGqgYosszZzgMwrgM4bw.png.webp",
        },
        {
          keys: 6,
          url: "http://31728769.s21i.faiusr.com/4/ABUIABAEGAAgt_SGqgYosMeqxwIweThB.png.webp",
        },
      ],
      timer: null,
      moveLeft: 0,
    };
  },
  methods: {
    move() {
      let liElements = document.getElementsByClassName("partners-content-carousel-item");
      this.timer = setInterval(() => {  
        if (Math.abs(this.moveLeft) % 295 === 0 && this.moveLeft !== 0) {
          this.imageList.push(item);
          this.moveLeft = 0;
        }
        this.moveLeft -= 5;
        for (let i = 0; i < liElements.length; i++) {
          liElements[i].style.transform = `translateX(${this.moveLeft}px)`;
        }
      }, 200);
    },
  },
  mounted() {
    this.move();
  },
};
</script>
<style scoped>
li {
  list-style: none;
}
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
  height: 1013px;
  background-image: url("http://31728769.s21i.faiusr.com/2/ABUIABACGAAgwvKHqgYokI7NHzCADzjYBA.jpg.webp");
  background-size: cover;
  font-family: 微软雅黑;
  background-position: center center;
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

.partners {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 575px;
}
.partners-content {
  height: 282px;
  font-size: 24px;
  font-family: 微软雅黑;
  font-weight: 700;
  text-align: center;
}
.partners-content-item {
  margin-top: 4px;
  font-size: 16px;
  color: rgb(153, 153, 153);
  font-weight: 400;
}

.partners-content-carousel {
  display: flex;
  height: 194px;
  max-width: 1556px;
  margin-top: 18px;
  overflow: hidden;
}

.partners-content-carousel-image {
  width: 295px;
  height: 194px;
  padding: 40px 17px;
}
</style>