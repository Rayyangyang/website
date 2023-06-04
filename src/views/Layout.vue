<template>
  <div style="font-size: 18px">
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      :ellipsis="false"
      @select="handleSelect"
      router
    >
      <el-menu-item index="0">
        <img src="@/assets/imgs/logo.png" class="sidebar-logo" />
      </el-menu-item>
      <div class="flex-grow" />
      <el-menu-item index="homePage">首页</el-menu-item>
      <el-menu-item index="productIntroduction">产品介绍</el-menu-item>
      <el-menu-item index="productionShow">成品展示</el-menu-item>
      <el-menu-item index="productionServer">产品服务</el-menu-item>
      <el-menu-item index="successCase">成功案例</el-menu-item>
      <el-menu-item index="aboutUs">关于我们</el-menu-item>
    </el-menu>
    <AppMain />
  </div>
</template>

<script lang="ts" setup>
import AppMain from "@/layout/components/AppMain.vue"
import { useRouter } from "vue-router"
import { ref, onMounted } from "vue"
const activeIndex = ref("homePage")

const router = useRouter()

router.beforeEach((to, from) => {
  activeIndex.value = to.fullPath.split("/")[1]
  console.log(22222, to)
})
onMounted(() => {
  console.log(1009999, location)
  const local = location.pathname.split("/")[1]
  activeIndex.value = local
})

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
.el-menu-item {
  line-height: 70px;
  font-size: 18px;
}
</style>
