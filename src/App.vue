<script lang="ts" setup>
import { ref } from 'vue'
import {  RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
// export default {
//   components: {
//     Menu
//   }
// }
const isCollapse = ref(false)
// const handleOpen = (key: string, keyPath: string[]) => {
//   console.log(key, keyPath)
// }
// const handleClose = (key: string, keyPath: string[]) => {
//   console.log(key, keyPath)
// }
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
  <Menu />
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
  background-color:#fdf6ec ;
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
  filter:alpha(Opacity=70);
  -moz-opacity:0.7;
  opacity:0.7;
} */
.el-aside{
  background-color:#000000;
  height: 100vh;
  filter:alpha(Opacity=40);
  -moz-opacity:0.4;
  opacity:0.4;
  /* background-image: url(./components/pexels-attila-szente-9512261.jpg);
  background-size:500%; */
}
</style>

