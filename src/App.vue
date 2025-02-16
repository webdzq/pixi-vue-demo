<template>
  <header class="header"></header>
  <div id="pixi-pro">

    <LeftMenu @left-menu-params="getLeftMenuParamsEvt" />
    <MainContent ref="mainRef" />
  </div>
</template>

<script setup>
import LeftMenu from './LeftMenu.vue';
import MainContent from './MainContent.vue';
import { provide, ref } from 'vue'
const mainRef = ref(null);
const sharedData = ref("初始共享数据");
// const changeSharedData = () => {
//   sharedData.value = "新的共享数据";
// };
// provide('sharedData', sharedData);
// let parentMessage = "这是来自父组件的消息";
const getLeftMenuParamsEvt = (msg) => {
  // parentMessage=msg
  sharedData.value = msg
  console.log('msg-', msg, sharedData.value)
  mainRef.value.getMenuVal(sharedData.value);
  // provide('sharedData', msg);
}

</script>

<style>
/* 这里可以添加全局的样式，比如设置整体页面的背景色等 */
body {
  margin: 0;
  padding: 0;
  background-color: #fff;
}

.header {
  width: 100vw;
  height: 5vh;
  background-color: #eee;
  position: fixed;
  top: 0;
  left: 0;
}
</style>