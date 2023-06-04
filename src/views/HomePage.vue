<template>
  <div class="home-page-wrapper">
    <div style="height: 800px; overflow: hidden; margin-bottom: 144px">
      <img src="../assets/imgs/home.png" alt="" style="height: 800px; width: 100%" />
    </div>
    <div class="company-info my-container">
      <div class="left">
        <h2 id="cInfo">公司简介</h2>
        <p style="text-align: justify; line-height: 40px">
          泸州泸南酒业有限公司坐落于中国白酒金三角核心腹地，公司传承活态酿造，在坚守传统古法的同时，坚持科学酿造，致力于打造最具价值的中国白酒专业供应链、中国白酒新品牌的孵化器，是一家拥有完整产业链的大型白酒生产企业。
        </p>
        <el-button
          style="
            width: 200px;
            line-height: 79px;
            color: #1c4695;
            font-size: 32px;
            height: 79px;
            border: 2px solid #1c4695;
            border-radius: 0;
          "
          @click="toAbout"
          >关于我们</el-button
        >
      </div>
      <div class="right">
        <img src="../assets/imgs/com-info.png" alt="" />
      </div>
    </div>

    <div class="img-list my-container">
      <img src="../assets/imgs/homeList1.png" alt="" />
      <img src="../assets/imgs/homeList2.png" alt="" />
      <img src="../assets/imgs/homeList3.png" alt="" />
      <img src="../assets/imgs/homeList4.png" alt="" />
    </div>

    <div class="hxjz" id="hxjz">
      <div class="my-container">
        <InfoTitle title="核心价值" desc="聚焦四大酒类核心业态，提供一体化解决方案" />

        <div style="display: flex">
          <div v-for="ele in hxzjList" :key="ele.title" class="hxjz-item">
            <img :src="ele.img" alt="" />
            <h2>{{ ele.title }}</h2>
            <p>{{ ele.desc }}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="cpjs" id="cpjs">
      <InfoTitle title="产品介绍" desc="聚焦四大酒类核心业态，提供一体化解决方案" />

      <div class="cpjs-list-wrapper">
        <div class="cpjs-list" :key="ele.title" v-for="(ele, i) in cpjsList">
          <div class="cpjs-img">
            <img :src="ele.img" alt="" />
          </div>
          <div class="cpjs-info">
            <h2>{{ ele.title }}</h2>
            <p>{{ ele.desc }}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="my-container" style="text-align: center; margin: 95px 0 152px">
      <el-button
        style="
          width: 200px;
          line-height: 79px;
          color: #1c4695;
          font-size: 32px;
          height: 79px;
          border: 2px solid #1c4695;
          border-radius: 0;
        "
        @click="toIns"
        >产品介绍</el-button
      >
    </div>

    <div class="cpfw" id="cpfw">
      <InfoTitle title="产品服务" desc="向客户提供从生产到销售再到运营的整套方案" />

      <div class="cpfw-wrapper my-container">
        <div class="cpfw-left">
          <div class="cpfw-title">
            <span>1. 生产</span>
            <i />
          </div>
          <p class="cpfw-desc">
            四川泸南酒类销售有限公司，是泸州最大的成品酒供应基地——泸州泸南酒业有限公司所属销售公司，专为客户提供酒质优异，酒体稳定，并具备一定稀缺性的产品。
          </p>
          <img src="../assets/imgs/cpfw1.png" alt="" />
        </div>
        <div class="cpfw-right">
          <div>
            <div class="cpfw-title">
              <span>2. 品牌</span>
              <i />
            </div>
            <p class="cpfw-desc">
              公司针对核心客户将提供全方位的品牌打造服务，包括市场规划，营销策划，品牌全案，销售支持以及雇员培训工作，解决客户实际销售问题，减少运营成本。
            </p>
          </div>
          <div>
            <div class="cpfw-title">
              <span>3. 运营</span>
              <i />
            </div>
            <p class="cpfw-desc">
              适用于所有类型客户，我们承诺，只要为本公司生产的产品，我们将提供产品周期内的日常管理服务，包括朋友圈素材，线上搭建，线下品鉴等专项服务
            </p>
          </div>
          <div>
            <div class="cpfw-title">
              <span>4. 开发</span>
              <i />
            </div>
            <p class="cpfw-desc">
              依托本公司强大的供应链保障能力，我们提供一站式的产品开发服务，从设计到选材，再到打样生产，免去大量繁琐环节，同时头部供应商保障质量管控，降低客户隐形成本，提高经营效力
            </p>
          </div>
          <div>
            <div class="cpfw-title">
              <span>5. 专属</span>
              <i />
            </div>
            <p class="cpfw-desc">针对公司长期合作的客户，我们将提供小批量专属定制酒服务，不限瓶型盒型规格，终身享受</p>
          </div>
        </div>
      </div>
    </div>

    <div class="my-container" style="text-align: center; margin: 95px 0 187px">
      <el-button
        style="
          width: 200px;
          line-height: 79px;
          color: #1c4695;
          font-size: 32px;
          height: 79px;
          border: 2px solid #1c4695;
          border-radius: 0;
        "
        @click="toser"
        >产品服务</el-button
      >
    </div>

    <div class="zj" id="zjtd">
      <div>
        <InfoTitle title="专家团队" desc="专家团队倾力打造，给你优质舒适服务" />
        <el-scrollbar wrap-class="test">
          <div class="scrollbar-flex-content">
            <div v-for="ele in zjList" :key="ele.img" class="scrollbar-demo-item">
              <div class="zj-img">
                <img :src="ele.img" alt="" />
              </div>
              <p>{{ ele.desc }}</p>
            </div>
          </div>
        </el-scrollbar>
      </div>
    </div>

    <div class="cpan zj" id="cpal">
      <InfoTitle title="产品案例" desc="为千万企业制定专属产品方案 " />

      <div style="margin-top: 83px">
        <el-scrollbar>
          <div class="scrollbar-flex-content">
            <div class="al-item" v-for="ele in alList" :key="ele.title">
              <div class="al-img">
                <img :src="ele.img" alt="" />
              </div>
              <div class="al-info">
                <h2>{{ ele.title }}</h2>
                <p>{{ ele.desc }}</p>
              </div>
            </div>
          </div>
        </el-scrollbar>
      </div>
      <div class="my-container" style="text-align: center; margin: 90px 0 138px">
        <el-button
          style="
            width: 200px;
            line-height: 79px;
            color: #1c4695;
            font-size: 32px;
            height: 79px;
            border: 2px solid #1c4695;
            border-radius: 0;
          "
          @click="toCpal"
          >产品案例</el-button
        >
      </div>
    </div>

    <!-- <Card :img="img1" title="test" boxType="123" bottleType="333" /> -->
    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue"
import { useRouter } from "vue-router"
import Footer from "./Footer.vue"
import Card from "./components/Card.vue"
import InfoTitle from "./InfoTitle.vue"
import hxjz1 from "../assets/imgs/hxjz1.png"
import hxjz2 from "../assets/imgs/hxjz2.png"
import hxjz3 from "../assets/imgs/hxjz3.png"

import cpjs1 from "../assets/imgs/cpjs1.png"
import cpjs2 from "../assets/imgs/cpjs2.png"
import cpjs3 from "../assets/imgs/cpjs3.png"
import cpjs4 from "../assets/imgs/cpjs4.png"

import zj1 from "../assets/imgs/zj1.png"
import zj2 from "../assets/imgs/zj2.png"
import zj3 from "../assets/imgs/zj3.png"
import zj4 from "../assets/imgs/zj4.png"
import zj5 from "../assets/imgs/zj5.png"

const router = useRouter()

const toAbout = () => {
  router.push("aboutUs")
}

const toIns = () => {
  router.push("productIntroduction")
}

const toser = () => {
  router.push("productionServer")
}
const toCpal = () => {
  router.push("successCase")
}

const hxzjList = ref([
  {
    title: "探路者",
    desc: "泸南酒业扩建于1977年，1997年划拨给泸州老窖集团，服务了最早一批泸州酒OEM客户，最早构建“酒+服务”销售体系，最早开始服务大中型非酒企客户，最早与央企实现联合经营",
    img: hxjz1
  },
  {
    title: "引领者",
    desc: "2020年孵化达州文化私域产品洲河醉，于第二年度开展招商引资战略，实现一站式服务，将全国白酒行业红海渠道市场细分为四大蓝海市场，引领白酒市场服务创新潮流",
    img: hxjz2
  },
  {
    title: "领航者",
    desc: "国内头部供应商资质护航白酒行业国内顶尖团队，大师技艺保障，第三方质量监督：酒厂综合检验检测中心，国家酒检中心，国家包检中心，高速无人灌装生产线，引领行业，国内知名快递、物流高速战略合作企业",
    img: hxjz3
  }
])

const cpjsList = ref([
  {
    title: "品牌联名酒",
    desc: "公司下辖多个重量级品牌，如“中垦飨味堂”、“待宾”、“洲河醉”、“尚缘”等，均可为客户提供二次品牌联名及孵化服务，降低销售门槛，引流增收",
    color: "#1C4695",
    bgColor: "#fff",
    img: cpjs1
  },
  {
    title: "地产文化酒",
    desc: "针对本地无规模化酒厂，且酒文化盛行，饮酒人数基数大，消费者对于浓香型白酒有较大认可的地区，公司可按照“洲河醉”模式进行全面复制，提供全案支持",
    color: "#1C4695",
    bgColor: "#fff",
    img: cpjs2
  },
  {
    title: "企业定制酒",
    desc: "为企业开发自有酒类产品，包括但不限于自用、赠送、销售类产品，提升企业形象，降低用酒成本，渠道创收",
    color: "#1C4695",
    bgColor: "#fff",
    img: cpjs3
  },
  {
    title: "私域圈层酒",
    desc: "帮助自有圈层客户开发私域高端产品，提供营销工具，设计销售逻辑，保障客户圈层私有性及变现能力",
    color: "#1C4695",
    bgColor: "#fff",
    img: cpjs4
  }
])

const zjList = ref([
  {
    img: zj1,
    desc: "中国白酒泰斗——胡永松教授，全国知名微生物与发酵专家，曾担任四川大学生物工程系系主任、四川大学食品与发酵工程研究所教授。兼任中国食品工业协会白酒专业委员会理事及技术顾问、四川省酿酒工业协会专家组副组长、四川省食品发酵学会名誉理事长、四川省省委、省政府科技顾问团顾问。"
  },
  {
    img: zj2,
    desc: "中国白酒青年专家——邹江鹏，泸州老窖集团与江南大学博士后，法国南特大学理学博士，中国四川大学工学博士，《酱香型白酒技术标准体系》主要制定者之一，高级工程师，国家一级品酒师，贵州大学、湖南农业大学、四川轻化工大学客座教授，青年白酒专家学者。贵州省白酒评委，贵州省科技厅白酒专家库成员，曾任贵州金沙窖酒酒业有限公司总工程师，天士力集团贵州国台酒业有限公司副总经理，泸州老窖集团首席技术营销官，重庆诗仙太白酒业总经理。"
  },
  {
    img: zj3,
    desc: "蒋欣振，四川大学 MBA ，泸南酒业供应链负责人。全日制硕士，国家一级品酒师，酒体设计师。曾就职于泸州老窖集团供应保障体系，十余年行业经验，擅长白酒私域产品的开发。成功孵化了待宾，洲河醉，尚缘，熊猫特曲，中垦飨味堂，甄品6号，贰柒柒等私域品牌。"
  },
  {
    img: zj4,
    desc: "邓锦文-四川泸南酒类销售有限公司副总经理，大客户事业部总监，泸南酒厂酒品牌大使，国家级品酒师，酒类技术营销培训讲师，具备多年讲师培训经验；负责企业营销端培训，白酒专业技能培训，“泸南品牌服务官计划”领衔人，对接泸南酒文化之旅项目。 "
  },
  {
    img: zj5,
    desc: "邓锦文-四川泸南酒类销售有限公司副总经理，大客户事业部总监，泸南酒厂酒品牌大使，国家级品酒师，酒类技术营销培训讲师，具备多年讲师培训经验；负责企业营销端培训，白酒专业技能培训，“泸南品牌服务官计划”领衔人，对接泸南酒文化之旅项目。 "
  }
])

const alList = ref([
  {
    title: "蒲丹「洲河醉」联合创始人",
    img: cpjs4,
    desc: "曾经我站在青藏高原守卫祖国边疆，退伍转业后是洲河醉让我找到了人生的第二个奋斗目标，感谢公司专业贴心的服务让我感受到做酒原来如此简单，从一位白酒爱好者到资深合伙人，只用了一年的时间，并确立了自己的核心市场，颇有收效。"
  },
  {
    title: "成都康弘药业集团股份有限公司",
    img: "",
    desc: "贵司通过强大的供应链保障能力，满足了集团的用酒需求，特别是专业的设计让公司的整体形象，让我们在日常接待及赠礼过程中提升了品牌形象，同时小批量销售也为员工和公司创造了价值，双方在未来将继续深入合作。"
  },
  {
    title: "郑常金定制酒服务商",
    img: "",
    desc: "泸南销售公司从酒体选择、产品设计、打样到最后定样，只花了一周时间，在后续的服务过程中，公司对我的支持处处体现，让我能放下负担，专注市场；作为民航界的一名老人，泸南销售公司的高效率让我回到了那些与天空相伴的日子。"
  },
  {
    title: "中国农垦控股",
    img: "",
    desc: "作为央企，我们强调服务社会，造福人民的理念，与泸南销售公司联名开发“中垦飨味堂-待宾酒”是我们“粮安天下，福慧民生”的品牌愿景，完成了将中国白酒联名共赢模式推上新高峰的整体战略布局。 "
  }
])
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
    flex: 1;
    height: 326px;
    overflow: hidden;
    img {
      width: 100%;
    }
  }
}

.img-list {
  display: flex;
  justify-content: space-between;
  margin-top: 57px;
  margin-bottom: 170px;
  > img {
    flex: 1;
    height: 179px;
    margin-right: 24px;
  }
  img:nth-last-child(1) {
    margin-right: 0;
  }
}

.hxjz {
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
      color: #1c4695;
      font-size: 36px;
      margin: 13px 0 7px;
    }
    p {
      font-size: 24px;
      text-align: justify;
      color: #4d4d4d;
    }
  }
}

.cpjs-list-wrapper {
  display: flex;
  margin-top: 86px;
  flex-wrap: wrap;
  .cpjs-img {
    margin-right: 40px;
  }
  h2 {
    font-weight: 400;
    font-size: 36px;
  }
  p {
    font-size: 24px;
  }
  > :nth-of-type(odd) {
    padding-left: 10%;
    display: flex;
    justify-content: flex-start;
    text-align: justify;
  }
  > :nth-of-type(even) {
    padding-right: 10%;
    text-align: justify;
  }
  > :nth-of-type(1) {
    padding-right: 79px;
    color: #1c4695;
  }
  > :nth-of-type(2) {
    background-color: #f2f2f2;
    padding-left: 79px;
    color: #1c4695;
  }
  > :nth-of-type(3) {
    background-color: #f2f2f2;
    padding-right: 79px;
    p {
      color: #4d4d4d;
    }
  }
  > :nth-of-type(4) {
    padding-left: 79px;
    p {
      color: #4d4d4d;
    }
  }
}
.cpjs-list {
  display: flex;
  width: 50%;
  height: 380px;
  align-items: center;
  p:nth-of-type(even) {
    margin-right: 85px;
  }
}

.cpfw {
  .cpfw-wrapper {
    display: flex;
    .cpfw-left {
      box-shadow: 2px 6px 4px 0 #cbe5ffff;
      border-radius: 10px;
      padding: 42px 26px 38px;
      width: 30%;
      margin-right: 21px;
      p {
        margin: 0px;
        text-align: justify;
        margin-bottom: 44px;
      }
      .cpfw-desc {
        font-size: 24px;
        color: #4d4d4d;
        line-height: 36px;
      }
    }
  }

  .cpfw-right {
    flex: 1;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    > div {
      width: calc(50% - 10px);
      background-color: #fff;
      box-shadow: 2px 6px 4px 0 #cbe5ffff;
      margin-bottom: 16px;
      border-radius: 10px;
      padding: 42px 26px 38px;
      margin-right: 20px;
    }
    > :nth-of-type(2) {
      margin-right: 0;
    }
    > :nth-of-type(4) {
      margin-right: 0;
      margin-bottom: 0px;
    }
    > :nth-of-type(3) {
      margin-bottom: 0px;
    }
    .cpfw-desc {
      font-size: 24px;
      color: #4d4d4d;
      line-height: 36px;
    }
  }

  .cpfw-title {
    display: inline-block;
    margin-bottom: 50px;
    position: relative;
    span {
      display: inline-block;
      font-size: 36px;
    }
    i {
      font-size: 24px;
      position: absolute;
      top: 60px;
      right: 0px;
      display: inline-block;
      width: 100%;
      height: 6px;
      background-color: #1c4695;
      border-radius: 6px;
    }
  }
}

.zj {
  padding-bottom: 30px;
  background-repeat: no-repeat;
  background-image: url("../assets/imgs/hxjz-bg.png");
  background-size: cover;
}

.scrollbar-flex-content {
  display: flex;
}
.scrollbar-demo-item {
  flex-shrink: 0;
  display: flex;
  width: 516px;
  background-color: #fff;
  text-align: center;
  border-radius: 4px;
  flex-direction: column;
  box-shadow: 2px 6px 4px 0 #cbe5ffff;
  padding: 0 29px;
  padding-top: 48px;
  margin: 0 22px;
  p {
    text-align: justify;
    font-size: 26px;
    margin: 0;
  }
  .zj-img {
    margin-bottom: 65px;
  }
}

.cpan {
  .al-item {
    flex-shrink: 0;
    display: flex;
    width: 953px;
    background-color: #fff;
    text-align: center;
    border-radius: 4px;
    box-shadow: 2px 6px 4px 0 #cbe5ffff;
    padding: 0 29px;
    padding-top: 48px;
    margin: 0 15px;
    .al-img {
      width: 50%;
      // img {
      //   width: 100%;
      // }
    }
    .al-info {
      width: 50%;
      text-align: justify;
      h2 {
        font-size: 36px;
        font-weight: 400;
      }
      p {
        font-size: 24px;
        color: #4d4d4d;
        line-height: 30px;
        font-weight: 200;
      }
    }
  }
}

:deep(.el-scrollbar__bar) {
  display: block !important;
}
:deep(.el-scrollbar__view) {
  padding-bottom: 40px;
}
</style>
