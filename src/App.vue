<script lang="ts" setup>
import { ref } from 'vue'
import {  RouterView } from 'vue-router'
const isCollapse = ref(false)
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
// const count = ref(0)
// const load = () => {
//   count.value += 2
// }
</script>
<template>
  <el-container class="home">
      <el-header>
        <el-container>
          <div style="text-align:center">
          <el-button color="#FFFFFF" circle="true" >～</el-button>
          </div>
        <div style="text-align:center">
          <el-button color="#95d475" circle="true" @click="isCollapse = !isCollapse" class="status">"  "</el-button>
          </div>
          <h1>Pnotes</h1>
      </el-container>
    </el-header>
      <el-container>
        <el-aside :width="isCollapse ? '64px' : '250px'">
          <!-- <div style="text-align:center">
          <el-button color="#95d475" circle="true" @click="isCollapse = !isCollapse" class="status">"  "</el-button>
          </div> -->
          <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px">
    <el-radio-button :label="false" >expand</el-radio-button>
    <el-radio-button :label="true">collapse</el-radio-button>
  </el-radio-group> -->
  <!-- <Menu /> -->
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

        </el-aside>
<!-- </el-container> -->
        <el-main>
          <!-- <RouterView></RouterView> -->
          <RouterView />
        </el-main>
      </el-container>
  </el-container>
</template>



<style>
#app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 110vh;
  /* background-color:#fdf6ec ; */
  /* background-image: url(./components/pexels-attila-szente-9512261.jpg);
  background-repeat: round; */
}

.el-header{
  background-color:#000000 ;
  color:snow;
  font-family: Georgia;
  font-style:oblique;
  font-size:2em;
  text-indent:0.5em
}
/* .el-main{
  background-color:#FFFFFF ;
  height: 100vh;
  filter:alpha(Opacity=80);
  -moz-opacity:0.8;
  opacity:0.8;
} */
.el-aside{
  background-color:#000000;
  height: 100vh;
  filter:alpha(Opacity=50);
  -moz-opacity:0.5;
  opacity:0.5;
  /* background-image: url(./components/pexels-attila-szente-9512261.jpg);
  background-size:500%; */
}
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
  color: #ffd04b;}
</style>

