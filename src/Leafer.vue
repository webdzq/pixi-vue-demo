<script setup lang="ts">
import {  Leafer } from 'leafer-ui'
   // 初始化 LeaferJS 实例
   const whiteboard = new Leafer({
        el: '#whiteboard-container', // 指定绘图容器
        width: 600, // 画布宽度
        height: 400, // 画布高度
        lineColor: 'black', // 线条颜色
        lineWidth: 5, // 线条宽度
        backgroundColor: 'white', // 画布背景颜色
    });
</script>

<template>
  <!-- <HelloWorld /> -->
  <div id="doodle-board">111</div>
</template>

<style scoped>
#doodle-board{
 border:1px solid red;
 background-color: white;
 width: 500px;
 height:500px;
}
</style>
