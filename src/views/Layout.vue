<template>
  <div>
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      :ellipsis="false"
      @select="handleSelect"
      router
    >
      <el-menu-item index="0">
        <!-- <img src="@/assets/imgs/logo.png" class="sidebar-logo" /> -->
      </el-menu-item>
      <div class="flex-grow" />
      <el-menu-item index="homePage">home</el-menu-item>
      <el-menu-item index="productIntroduction">productIntroduction</el-menu-item>
      <el-menu-item index="productionShow">productionShow</el-menu-item>
      <el-menu-item index="productionServer">productionServer</el-menu-item>
      <el-menu-item index="successCase">successCase</el-menu-item>
      <el-menu-item index="aboutUs">aboutUs</el-menu-item>
    </el-menu>
    <AppMain />
  </div>
</template>

<script lang="ts" setup>
import AppMain from "@/layout/components/AppMain.vue"

import { ref } from "vue"

const activeIndex = ref("1")
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<style>
.el-menu-demo {
  padding: 0 10%;
  border-bottom: none;
}
.flex-grow {
  flex-grow: 1;
}
</style>
