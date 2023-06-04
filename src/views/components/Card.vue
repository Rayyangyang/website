<template>
  <div class="card-wrapper">
    <div class="logo"><img src="../../assets/imgs/logo.png" alt="" /></div>
    <div class="img-wrapper">
      <img :src="props.img" alt="" style="width: 608px" />
    </div>
    <table border="1" style="border-collapse: collapse">
      <tr>
        <td class="table-title">品名</td>
        <td colspan="3" style="padding-left: 20px" v-if="!props.design">{{ props.title }}</td>
        <td :colspan="0" style="text-align: center" v-else>{{ props.title }}</td>
        <td class="table-title" v-show="props.design">设计者</td>
        <td style="text-align: center" v-show="props.design">{{ props.design }}</td>
      </tr>
      <tr>
        <td class="table-title">瓶型</td>
        <td colspan="3" style="padding-left: 20px" v-if="!props.boxType">{{ props.bottleType }}</td>
        <td :colspan="0" style="text-align: center" v-else>{{ props.bottleType }}</td>
        <td class="table-title" v-show="props.boxType">盒型</td>
        <td style="text-align: center" v-show="props.boxType">{{ props.boxType }}</td>
      </tr>
    </table>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(["img", "title", "boxType", "bottleType", "design"])
</script>

<style scoped lang="scss">
.card-wrapper {
  // width: 708px;
  width: 50%;
  height: 764px;
  background-color: #fff;
  margin-bottom: 87px;
}
.img-wrapper {
  width: 600px;
  img {
    width: 600px;
  }
}
.logo {
  width: 608px;
}
table {
  // width: 608px;
  width: 80%;
  font-size: 18px;
  .table-title {
    width: 80px;
    text-align: center;
    background-color: #c7221c;
    color: #fff;
  }
}
</style>
