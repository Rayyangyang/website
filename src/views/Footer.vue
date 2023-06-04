<template>
  <footer class="footer my-container">
    <div class="footer-wrapper">
      <div class="footer-content">
        <div class="footer-section">
          <h3>首页</h3>
          <ul>
            <li><a href="/homePage#cInfo">公司简介</a></li>
            <li><a href="/homePage#hxjz">核心价值</a></li>
            <li><a href="/homePage#cpjs">产品介绍</a></li>
            <li><a href="/homePage#cpfw">产品服务</a></li>
            <li><a href="/homePage#zjtd">专家团队</a></li>
            <li><a href="/homePage#cpal">产品案例</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>产品介绍</h3>
          <ul>
            <li><a href="/productIntroduction#qydz">企业定制</a></li>
            <li><a href="/productIntroduction#dcwh">地产文化</a></li>
            <li><a href="/productIntroduction#pplm">品牌联名</a></li>
            <li><a href="/productIntroduction#syqc">私域圈层</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>产品服务</h3>
          <ul>
            <li><a href="/productionServer#fwnr">服务内容</a></li>
            <li><a href="/productionServer#fwlc">服务流程</a></li>
            <li><a href="/productionServer#fwhx">服务核心</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>成功案例</h3>
          <ul>
            <li><a href="/successCase#qydz1">企业定制</a></li>
            <li><a href="/successCase#">地产文化</a></li>
            <li><a href="/successCase#">品牌联名</a></li>
            <li><a href="/successCase#">私域圈层</a></li>
            <li><a href="/successCase#">行业定制</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>关于我们</h3>
          <ul>
            <li><a href="/aboutUs#gsjj">公司简介</a></li>
            <li><a href="/aboutUs#fzlc">发展历程</a></li>
            <li><a href="/aboutUs#fwys">服务优势</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-right">
        <p style="font-size: 18px">扫一扫了解更多</p>
        <div>
          <div class="qr-code">
            <img src="../assets/imgs/ercode.png" alt="二维码" style="height: 222px; width: 222px" />
          </div>
          <div class="production-info">
            <p>产地：中国四川泸洲</p>
            <p>生产厂家：泸州泸南酒业有限公司</p>
            <p>生产地址：江阳区黄舣镇酒业集中发展区</p>
            <p>负责人：李先生</p>
            <p>联系电话：028-82871724</p>
            <p>邮件地址：569224462@qq.com</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
import { useRouter } from "vue-router"
const router = useRouter()
const toQy = () => {
  router.push("/productIntroduction?#qydz")
}
</script>
<style scoped lang="scss">
.footer {
  background-color: #4d4d4d;
  padding-top: 60px;
  padding-bottom: 68px;
  color: #fff;
}

.footer-wrapper {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.footer-section {
  // /* flex-basis: 16%; */
  // width: 72px;
  margin-bottom: 20px;
  margin-right: 46px;
  h3 {
    font-size: 18px;
    text-align: center;
    margin-bottom: 32px;
  }
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

ul li {
  margin-bottom: 19px;
}

ul li a {
  color: #fff;
  text-decoration: none;
  font-weight: 200;
}

.footer-right {
  > div {
    display: flex;
    align-items: flex-start;
  }
}

.qr-code img {
  height: auto;
  margin-right: 29px;
}

.production-info p {
  margin: 15px 0;
  font-size: 18px;
  font-weight: 200;
}
</style>
