<script lang="ts" setup>
import { ref } from 'vue'
const isCollapse = ref(false)
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>
<template>
<el-menu
    default-active="2"
    class="el-menu-vertical-demo"
    :collapse="isCollapse"
    @open="handleOpen"
    @close="handleClose"
    router="true"
    text-color="#95d475"
    active-text-color="#ffd04b"
  >
    <el-sub-menu index="1">
      <template #title>
        <!-- <el-link type="success">马</el-link> -->
        <RouterLink to="/1">马</RouterLink>
        <span><RouterLink to="/1">克思主义基本原理</RouterLink></span>
        <!-- <span>克思主义基本原理</span> -->
      </template>
        <el-menu-item index="1-1">世界的物质性及发展规律</el-menu-item>
        <el-menu-item index="1-2">实践与认识及其发展规律</el-menu-item> 
        <el-menu-item index="1-3">人类社会及其发展规律</el-menu-item>
        <el-menu-item index="1-4">资本主义的本质和规律</el-menu-item>
      <!-- <el-sub-menu index="1-4">
        <template #title><span>item four</span></template>
        <el-menu-item index="1-4-1">item one</el-menu-item>
      </el-sub-menu> -->
      <el-menu-item index="1-5">资本主义的发展及其趋势</el-menu-item>
      <el-menu-item index="1-6">社会主义的发展及其规律</el-menu-item>
      <el-menu-item index="1-7">共产主义崇高理想及其最终实现</el-menu-item>
    </el-sub-menu>
    <el-menu-item index="2">
      <el-link type="success">毛</el-link>
      <template #title>泽东思想和中国特色社会主义</template>
    </el-menu-item>
    <el-menu-item index="3" >
      <el-link type="success">近</el-link>
      <template #title>代史纲要</template>
    </el-menu-item>
    <el-menu-item index="4">
      <el-link type="success">思</el-link>
      <template #title>想道德与法制</template>
    </el-menu-item>
  </el-menu>
</template>
<style>
.el-menu{
  background-color:transparent !important;
}
/* routerlink默认颜色 */
a{
  text-decoration: none;
  color: #95d475;
}
.router-link-active {
  text-decoration: none;
  color: #ffd04b;
}</style>