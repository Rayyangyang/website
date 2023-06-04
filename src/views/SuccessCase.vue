<template>
  <div class="success-wrapper">
    <div style="height: 800px; overflow: hidden; margin-bottom: 144px">
      <img src="../assets/imgs/success-bg.png" alt="" style="height: 800px; width: 100%" />
    </div>

    <div class="success-content my-container">
      <div class="left-nav">
        <div v-for="(ele, i) in navLis" :key="i" :class="curI == i ? 'active' : ''" class="nav-item" @click="curI = i">
          {{ ele }}
        </div>
      </div>
      <div class="right-content">
        <div v-for="ele in contents" :key="ele.title">
          <div class="img">
            <img :src="ele.img" alt="" />
          </div>
          <div class="content">
            <h2>{{ ele.title }}</h2>
            <p>{{ ele.desc }}</p>
          </div>
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue"
import Footer from "./Footer.vue"

import pi4 from "../assets/imgs/pi4.png"

onMounted(() => {
  document.documentElement.scrollTop = 0
  const local = location
  if (local.hash) document.querySelector(local.hash).scrollIntoView()
})

const navLis = ref(["企业定制酒", "地域文化酒", "品牌联名酒", "思域圈层酒", "行业定制酒"])
const contents = ref([
  {
    title: "蒲丹「洲河醉」联合创始人",
    img: pi4,
    desc: "曾经我站在青藏高原守卫祖国边疆，退伍转业后是洲河醉让我找到了人生的第二个奋斗目标，感谢公司专业贴心的服务让我感受到做酒原来如此简单，从一位白酒爱好者到资深合伙人，只用了一年的时间，并确立了自己的核心市场，颇有收效。"
  },
  {
    title: "成都康弘药业集团股份有限公司",
    img: pi4,
    desc: "贵司通过强大的供应链保障能力，满足了集团的用酒需求，特别是专业的设计让公司的整体形象，让我们在日常接待及赠礼过程中提升了品牌形象，同时小批量销售也为员工和公司创造了价值，双方在未来将继续深入合作。"
  }
])

const curI = ref(0)
</script>

<style scoped lang="scss">
.success-content {
  display: flex;
  .left-nav {
    > div {
      flex: 1;
      width: 220px;
      height: 107px;
      text-align: center;
      line-height: 107px;
      border-radius: 10px;
      background-color: #f2f8ff;
      margin-bottom: 59px;
      color: #1c4695;
      font-size: 36px;
      cursor: pointer;
      user-select: none;
    }
    .active {
      background-color: #1c4695;
      color: #fff;
    }
  }
}

.right-content {
  margin-left: 122px;
  > div {
    margin-bottom: 57px;
    width: 1098px;
    border: 1px solid #000000ff;
    background: #ffffffff;
    box-shadow: 0 4px 4px 0 #f5f5f5ff;
    border-radius: 16px;
    .img {
      text-align: center;
    }
    .content {
      padding: 20px 50px 20px 50px;
      h2 {
        font-size: 42px;
        margin: 0;
      }
      p {
        font-size: 32px;
        color: #4d4d4d;
        font-weight: 200;
        line-height: 50px;
      }
    }
  }
}
</style>
