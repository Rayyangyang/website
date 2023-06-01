<template>
  <div class="home-page-wrapper">
    <el-carousel trigger="click" height="150px">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3 class="small justify-center" text="2xl">{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
    <div class="company-info my-container">
      <div class="left">
        <h2>公司简介</h2>
        <p>
          泸州泸南酒业有限公司坐落于中国白酒金三角核心腹地，公司传承活态酿造，在坚守传统古法的同时，坚持科学酿造，致力于打造最具价值的中国白酒专业供应链、中国白酒新品牌的孵化器，是一家拥有完整产业链的大型白酒生产企业。
        </p>
        <el-button>了解更多</el-button>
      </div>
      <div class="right">
        <img src="../assets/imgs/com-info.png" alt="" />
      </div>
    </div>
    <Card :img="img1" title="test" boxType="123" bottleType="333" />
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Footer from "./Footer.vue"
import Card from "./components/Card.vue"
import img1 from "../assets/imgs/img2.png"
</script>

<style scoped lang="scss">
.company-info {
  display: flex;
  align-items: flex-start;
  > div {
    width: 50%;
  }
  .left {
    font-size: 24px;
    h2 {
      margin-top: 10px;
      font-size: 42px;
      margin-bottom: 17px;
    }
    p {
      margin-top: 17px;
      font-weight: 400;
      color: #4d4d4d;
      font-family: "Source Han Serif SC";
    }
  }
  .right {
    margin-left: 122px;
    width: 708px;
    height: 326px;
  }
}
</style>
