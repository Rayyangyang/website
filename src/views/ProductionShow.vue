<template>
  <div class="pd-show">
    <div style="height: 800px; overflow: hidden; margin-bottom: 71px">
      <img src="../assets/imgs/pd.png" alt="" style="height: 800px; width: 100%" />
    </div>
    <InfoTitle title="成品展示" desc="十多款优良产品供您挑选" />

    <div class="card my-container">
      <Card
        v-for="ele in cardList"
        :key="ele.title"
        :img="ele.img"
        :title="ele.title"
        :bottleType="ele.bottleType"
        :boxType="ele.boxType"
        :design="ele.design"
      />
    </div>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue"
import InfoTitle from "./InfoTitle.vue"
import Card from "@/views/components/Card.vue"
import Footer from "./Footer.vue"
import pds1 from "../assets/imgs/pds1.png"
import pds2 from "../assets/imgs/pds2.png"
import pds3 from "../assets/imgs/pds3.png"
import pds4 from "../assets/imgs/psd4.png"
import pds5 from "../assets/imgs/psd5.png"
import pds6 from "../assets/imgs/psd6.png"
import pds7 from "../assets/imgs/psd7.png"
import pds8 from "../assets/imgs/psd8.png"
import pds9 from "../assets/imgs/psd9.png"
import pds10 from "../assets/imgs/psd10.png"
import pds11 from "../assets/imgs/psd11.png"
import pds12 from "../assets/imgs/psd12.png"
import pds13 from "../assets/imgs/psd13.png"
import pds14 from "../assets/imgs/psd14.png"
import pds15 from "../assets/imgs/psd15.png"
import pds16 from "../assets/imgs/psd16.png"
const cardList = ref([
  {
    img: pds1,
    title: "特宾王酒",
    bottleType: "晶白玻璃瓶",
    boxType: "天地盖卡盒"
  },
  {
    img: pds2,
    title: "特宾王酒·手作一号",
    bottleType: "条纹玻璃瓶",
    boxType: "天地盖卡盒"
  },
  {
    img: pds3,
    title: "52度277酒",
    bottleType: "方形瓶",
    design: "徐婧",
    boxType: "天地盖卡盒"
  },
  {
    img: pds4,
    title: "水亨主题会议酒·坚劲",
    bottleType: "方形玻璃瓶",
    design: "徐婧",
    boxType: "书本盒"
  },
  {
    img: pds5,
    title: "水亨25周年纪念酒",
    bottleType: "圆柱玻璃瓶",
    design: "徐婧",
    boxType: "书盒"
  },
  {
    img: pds6,
    title: "婚庆定制酒",
    bottleType: "方型玻璃瓶",
    design: "庞宇",
    boxType: "书本盒"
  },
  {
    img: pds7,
    title: "洲河醉·特曲酒",
    bottleType: "60版玻璃瓶",
    design: "",
    boxType: "书盒"
  },
  {
    img: pds8,
    title: "52度特曲酒",
    bottleType: "60版玻璃瓶",
    design: "徐婧",
    boxType: "卡盒"
  },
  {
    img: pds9,
    title: "臻品6号特曲酒",
    bottleType: "60版玻璃瓶",
    design: "徐婧、庞宇",
    boxType: "卡盒"
  },
  {
    img: pds10,
    title: "52度远喝酒",
    bottleType: "圆柱瓶",
    design: "徐婧",
    boxType: "书本盒"
  },
  {
    img: pds11,
    title: "中垦味堂·特宾酒A30",
    bottleType: "圆柱玻璃瓶",
    design: "徐婧、庞宇",
    boxType: "上翻盖盒"
  },
  {
    img: pds12,
    title: "中垦味堂·特宾酒A60",
    bottleType: "圆柱玻璃瓶（金）",
    design: "徐婧、庞宇",
    boxType: "书本盒"
  },
  {
    img: pds13,
    title: "中垦味堂·特宾酒A90",
    bottleType: "圆柱玻璃瓶（蓝）",
    design: "徐婧、庞宇",
    boxType: "仿皮书本预扣盒"
  },
  {
    img: pds14,
    title: "洲河醉·义",
    bottleType: "圆柱喷釉瓶（金）",
    design: "徐婧、庞宇",
    boxType: "仿皮书本预扣盒"
  },
  {
    img: pds15,
    title: "洲河醉·明",
    bottleType: "圆柱喷釉瓶（蓝）",
    design: "",
    boxType: "天地盖卡盒"
  },
  {
    img: pds16,
    title: "私人订制酒",
    bottleType: "方型玻璃瓶",
    design: "徐婧",
    boxType: ""
  }
])
</script>

<style scoped lang="scss">
.card {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
