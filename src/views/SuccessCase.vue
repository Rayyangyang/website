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
        <div v-if="contents[curI].content.length > 0">
          <div v-for="ele in contents[curI].content" :key="ele.title">
            <div class="img">
              <img :src="ele.img" alt="" />
            </div>
            <div class="content">
              <h2>{{ ele.title }}</h2>
              <p>{{ ele.desc }}</p>
            </div>
          </div>
        </div>
        <div v-else class="no-data">暂无数据</div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue"
import Footer from "./Footer.vue"

import pi4 from "../assets/imgs/pi4.png"
import successImg1 from "../assets/imgs/successImg1.png"
import successImg2 from "../assets/imgs/successImg2.png"
import successImg3 from "../assets/imgs/successImg3.png"
import successImg4 from "../assets/imgs/successImg4.png"

onMounted(() => {
  document.documentElement.scrollTop = 0
  const local = location
  if (local.hash) document.querySelector(local.hash).scrollIntoView()
})

const navLis = ref(["企业定制酒", "地域文化酒", "品牌联名酒", "思域圈层酒", "行业定制酒"])
const contents = ref([
  {
    title: "企业定制酒-中南海运",
    content: [
      {
        title: "企业定制酒-中南海运",
        img: successImg1,
        desc: "作为全球最大的集装箱码头运营商，中国远洋海运集团完善的全球化服务筑就了网络服务优势与品牌优势。集团集采平台与泸南酒业合作开发“中国泸州特曲酒”酒体优质，设计简洁大方，备受集团成员青睐。"
      },
      {
        title: "蒲丹「洲河醉」联合创始人",
        img: successImg2,
        desc: "曾经我站在青藏高原守卫祖国边疆，退伍转业后是洲河醉让我找到了人生的第二个奋斗目标，感谢公司专业贴心的服务让我感受到做酒原来如此简单，从一位白酒爱好者到资深合伙人，只用了一年的时间，并确立了自己的核心市场，颇有收效。"
      },
      {
        title: "成都康弘药业集团股份有限公司",
        img: successImg3,
        desc: "贵司通过强大的供应链保障能力，满足了集团的用酒需求，特别是专业的设计让公司的整体形象，让我们在日常接待及赠礼过程中提升了品牌形象，同时小批量销售也为员工和公司创造了价值，双方在未来将继续深入合作。"
      },
      {
        title: "中国农垦控股",
        img: successImg4,
        desc: "作为央企，我们强调服务社会，造福人民的理念，与泸南销售公司联名开发“中垦飨味堂-待宾酒”是我们“粮安天下，福慧民生”的品牌愿景，完成了将中国白酒联名共赢模式推上新高峰的整体战略布局。"
      }
    ]
  },
  {
    title: "地域文化酒",
    content: []
  },
  {
    title: "品牌联名酒",
    content: []
  },
  {
    title: "思域圈层酒",
    content: []
  },
  {
    title: "行业定制酒",
    content: []
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

.no-data {
  border: none !important;
  font-size: 40px;
  text-align: center;
  line-height: 200px;
}
</style>
