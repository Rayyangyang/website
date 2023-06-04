<template>
  <div>
    <h3 style="text-align: center; font-size: 42px; font-weight: 500; margin-bottom: 0">{{ props.title }}</h3>
    <p style="text-align: center; font-size: 20px; margin-top: 16px">{{ props.desc }}</p>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(["title", "desc"])
</script>

<style scoped lang="scss"></style>
