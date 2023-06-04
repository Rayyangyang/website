<template>
  <div class="about-wrapper">
    <div style="height: 800px; overflow: hidden; margin-bottom: 144px">
      <img src="../assets/imgs/about.png" alt="" style="height: 800px; width: 100%" />
    </div>

    <div class="bg-wrapper" id="gsjj">
      <div class="bg-line">
        <div class="bg1">
          <img src="../assets/imgs/line-bg1.png" alt="" />
        </div>
        <div class="bg2">
          <h2>公司简介</h2>
          <p>
            泸州泸南酒业有限公司坐落于中国白酒金三角核心腹地，公司传承活态酿造，在坚守传统古法的同时，坚持科学酿造，致力于打造最具价值的中国白酒专业供应链、中国白酒新品牌的孵化器，是一家拥有完整产业链的大型白酒生产企业。
          </p>
        </div>
        <div class="bg3">
          <p>公司年产优质纯粮固态原酒1.5万吨，年灌装生产能力3万吨，综合储酒能力10万吨，总产值逾10亿元。</p>
        </div>
      </div>
    </div>

    <InfoTitle title="发展历程" desc="40年建厂历史，8年行业深耕，我们一直在路上 " id="fzlc" />

    <div class="jf-wrapper my-container">
      <div class="jf">
        <div class="jf-bg">
          <h2>1977</h2>
          <p>国营石梁曲酒厂始建</p>
        </div>
        <div class="imgup">
          <img src="../assets/imgs/lineup.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>1987</h2>
          <p>泸南大曲获得四川省优质产品奖</p>
        </div>
        <div class="imgdown">
          <img src="../assets/imgs/linedown.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>1988</h2>
          <p>获得农业部优质产品称号</p>
        </div>
        <div class="imgup">
          <img src="../assets/imgs/lineup.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>1997</h2>
          <p>泸州市酿酒厂整体划拨给泸州最大国有企业</p>
        </div>
        <div class="imgdown">
          <img src="../assets/imgs/linedown.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>2013</h2>
          <p>石洞酿酒基地投建</p>
        </div>
        <div class="imgdown1">
          <img src="../assets/imgs/linedown1.png" alt="" />
        </div>
      </div>

      <div class="jf jf-copy">
        <div class="jf-bg">
          <h2>2020</h2>
          <p>达州区域品牌“洲河醉”孵化上市</p>
        </div>
        <div class="imgdown">
          <img src="../assets/imgs/linedown.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>2016</h2>
          <p>石洞酿酒基地正式投产</p>
        </div>
        <div class="imgup">
          <img src="../assets/imgs/lineup.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>2015.6</h2>
          <p>开发出第一款企业定制酒“尚缘”</p>
        </div>
        <div class="imgdown">
          <img src="../assets/imgs/linedown.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>2015.1</h2>
          <p>泸南销售酒类销售新模式 搭建</p>
        </div>
        <div class="imgup">
          <img src="../assets/imgs/lineup.png" alt="" />
        </div>
        <div class="jf-bg">
          <h2>2014</h2>
          <p>自营品牌“待宾王、待宾一号”上线</p>
        </div>
      </div>
    </div>

    <InfoTitle title="服务优势" desc="行业深耕多年，优势遥遥领先 " id="fwys" />

    <div class="my-container fwys" style="margin-bottom: 100px">
      <div style="display: flex">
        <div v-for="ele in hxzjList" :key="ele.title" class="hxjz-item">
          <img :src="ele.img" alt="" />
          <h2>{{ ele.title }}</h2>
          <p>{{ ele.desc }}</p>
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue"
import Footer from "./Footer.vue"
import InfoTitle from "./InfoTitle.vue"

import s1 from "../assets/imgs/s1.png"
import s2 from "../assets/imgs/s2.png"
import s3 from "../assets/imgs/s3.png"
onMounted(() => {
  document.documentElement.scrollTop = 0
  const local = location
  if (local.hash) document.querySelector(local.hash).scrollIntoView()
})
const hxzjList = ref([
  {
    title: "100万酒友的信赖之选",
    desc: "截止2021年底，公司所服务的酒友突破1000000人次",
    img: s1
  },
  {
    title: "100%本科及以上学历员工",
    desc: "产品的专业服务支持 ",
    img: s2
  },
  {
    title: "泸州千亿级供应链保障",
    desc: "成都销售服务中心，泸南双生产中心泸州供应链保障中心；三位一体共筑酒业新商业模式。 ",
    img: s3
  }
])
</script>

<style scoped lang="scss">
.bg-wrapper {
  padding-bottom: 140px;
  display: flex;
  justify-content: center;
}
.bg-line {
  background: url("../assets/imgs/aboutLine.png");
  width: 1122px;
  height: 1100px;
  position: relative;
  background-size: 100% 100% !important;
}
.bg1 {
  width: 1239px;
  height: 824px;
  position: absolute;
  left: -200px;
  top: 50px;
  img {
    width: 100%;
    height: 100%;
  }
}

.bg2 {
  background: url("../assets/imgs/about-bg2.png");
  width: 673px;
  height: 464px;
  background-size: 100% 100% !important;
  position: absolute;
  right: -110px;
  top: 580px;
  color: #fff;
  padding: 40px;
  padding-left: 80px;
  h2 {
    font-size: 42px;
  }
  p {
    font-size: 32px;
    font-weight: 200;
    line-height: 40px;
  }
}
.bg3 {
  background: url("../assets/imgs/aboutbg3.png");
  width: 535px;
  height: 340px;
  background-size: 100% 100% !important;
  position: absolute;
  right: 500px;
  top: 780px;
  color: #fff;
  padding: 40px;
  p {
    font-size: 32px;
    font-weight: 200;
    line-height: 44px;
  }
}

.jf {
  display: flex;
  align-items: center;
  position: relative;
  .jf-bg {
    background: url("../assets/imgs/jtcenter.png") no-repeat;
    background-size: 100% 100%;
    width: 180px;
    height: 180px;
    padding-left: 20px;
    padding-right: 20px;
    flex: 1;
    h2 {
      font-size: 32px;
      margin-top: 0px;
      color: #1c4695;
      text-align: center;
      padding-top: 40px;
      font-weight: 400;
      margin-bottom: 0px;
    }
    p {
      font-size: 20px;
      color: #1c4695;
      text-align: center;
      font-weight: 200;
      margin-top: 10px;
    }
  }
  .imgup {
    margin-top: -60px;
  }
  .imgdown {
    margin-top: 60px;
  }
  .imgdown1 {
    position: absolute;
    right: -75px;
    top: 80px;
  }
}
.jf-copy {
  margin-top: 130px;
}
.fwys {
  padding-top: 140px;
  padding-bottom: 30px;
  background-repeat: no-repeat;
  background-image: url("../assets/imgs/hxjz-bg.png");
  background-size: cover;
  .hxjz-item {
    flex: 1;
    padding: 20px;
    background-color: #fff;
    margin-right: 24px;
    box-shadow: 2px 6px 6px 0 #cbe5ffff;
    border-radius: 16px;
    img {
      width: 100%;
    }
    h2 {
      text-align: center;
      color: #000;
      font-size: 36px;
      margin: 13px 0 7px;
    }
    p {
      font-size: 24px;
      text-align: justify;
      color: #4d4d4d;
      font-weight: 200;
    }
  }
}
</style>
