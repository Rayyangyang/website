<template>
  <div class="product">
    <div style="height: 800px; overflow: hidden; margin-bottom: 71px">
      <img src="../assets/imgs/product.png" alt="" style="height: 800px; width: 100%" />
    </div>

    <div class="list my-container">
      <div class="list-item1 bg1">企业定制酒</div>
      <div class="list-item1 bg2">地产文化酒</div>
      <div class="list-item1 bg3">品牌联名酒</div>
      <div class="list-item1 bg4">私域圈层酒</div>
    </div>

    <div class="p-list my-container">
      <div>
        <div class="cpjs-list-wrapper">
          <div class="cpjs-list" id="pplm">
            <div class="cpjs-img">
              <img src="../assets/imgs/pi1.png" alt="" />
            </div>
            <div class="cpjs-info">
              <h2>品牌联名酒</h2>
              <p>
                公司下辖多个重量级品牌，如“中垦飨味堂”、“待宾”、“洲河醉”、“尚缘”等，均可为客户提供二次品牌联名及孵化服务，降低销售门槛，引流增收
              </p>
            </div>
          </div>
          <div class="cpjs-list" id="dcwh">
            <div class="cpjs-info">
              <h2>地产文化酒</h2>
              <p>
                针对本地无规模化酒厂，且酒文化盛行，饮酒人数基数大，消费者对于浓香型白酒有较大认可的地区，公司可按照“洲河醉”模式进行全面复制，提供全案支持
              </p>
            </div>
            <div class="cpjs-img">
              <img src="../assets/imgs/pi2.png" alt="" />
            </div>
          </div>
          <div class="cpjs-list" id="qydz">
            <div class="cpjs-img">
              <img src="../assets/imgs/pi3.png" alt="" />
            </div>
            <div class="cpjs-info">
              <h2>企业定制酒</h2>
              <p>为企业开发自有酒类产品，包括但不限于自用、赠送、销售类产品，提升企业形象，降低用酒成本，渠道创收</p>
            </div>
          </div>
          <div class="cpjs-list" id="syqc">
            <div class="cpjs-info">
              <h2>私域圈层酒</h2>
              <p>帮助自有圈层客户开发私域高端产品，提供营销工具，设计销售逻辑，保障客户圈层私有性及变现能力</p>
            </div>
            <div class="cpjs-img">
              <img src="../assets/imgs/pi4.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="pibg">
      <img src="../assets/imgs/pibg1.png" alt="" />
    </div>
    <div class="pibg2">
      <img src="../assets/imgs/pibg2.png" alt="" />
    </div>

    <Footer />
  </div>
</template>

<script setup lang="ts">
import Footer from "./Footer.vue"
import { onMounted } from "vue"

onMounted(() => {
  document.documentElement.scrollTop = 0
  const local = location
  if (local.hash) document.querySelector(local.hash).scrollIntoView()
})
</script>

<style scoped lang="scss">
.list {
  margin-bottom: 221px;
  display: flex;
  justify-content: space-between;
  position: relative;
  z-index: 2;
}
.list-item1 {
  width: 342px;
  padding: 102px 0;
  text-align: center;
  font-size: 40px;
  color: #fff;
  background-size: contain !important;
  ::marker {
    content: "";
    display: none;
  }
}
.bg1 {
  background: url("../assets/imgs/p1.png") no-repeat;
}
.bg2 {
  background: url("../assets/imgs/p2.png") no-repeat;
}
.bg3 {
  background: url("../assets/imgs/p3.png") no-repeat;
}
.bg4 {
  background: url("../assets/imgs/p4.png") no-repeat;
}

.cpjs-list-wrapper {
  display: flex;
  flex-wrap: wrap;

  .cpjs-img {
    margin-right: 40px;
  }
  h2 {
    font-weight: 400;
    font-size: 48px;
    margin-bottom: 47px;
  }
  p {
    font-size: 36px;
    font-weight: 200;
    line-height: 60px;
  }
  > div {
    padding-left: 10%;
    display: flex;
    justify-content: flex-start;
    text-align: justify;
    box-shadow: 0 6px 6px 0 #00000012;
    background-color: #fff;
    padding: 44px 111px 44px 75px;
    align-items: center;
    margin-bottom: 100px;
  }
}
.p-list {
  position: relative;
  z-index: 2;
}
.product {
  position: relative;
  z-index: 2;
}
.pibg {
  position: absolute;
  top: 1820px;
  left: 0;
  z-index: 0;
}
.pibg2 {
  position: absolute;
  top: 2820px;
  right: -80px;
  z-index: 0;
}
</style>
