<template>
  <div class="card-wrapper">
    <div class="logo"><img src="../../assets/imgs/logo.png" alt="" /></div>
    <div class="img-wrapper">
      <img :src="props.img" alt="" />
    </div>
    <table border="1" style="border-collapse: collapse">
      <tr>
        <td class="table-title">品名</td>
        <td colspan="3" style="padding-left: 20px">{{ props.title }}</td>
      </tr>
      <tr>
        <td class="table-title">瓶型</td>
        <td style="text-align: center">{{ props.bottleType }}</td>
        <td class="table-title">盒型</td>
        <td style="text-align: center">{{ props.boxType }}</td>
      </tr>
    </table>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(["img", "title", "boxType", "bottleType"])
</script>

<style scoped lang="scss">
.card-wrapper {
  width: 708px;
  height: 764px;
}
.img-wrapper {
  width: 600px;
  img {
    width: 600px;
  }
}
table {
  width: 680px;
  font-size: 18px;
  .table-title {
    width: 80px;
    text-align: center;
    background-color: red;
    color: #fff;
  }
}
</style>
