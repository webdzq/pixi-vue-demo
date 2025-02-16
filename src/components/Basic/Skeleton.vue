<script setup lang="js">
import { onMounted } from "vue";
import * as PIXI from 'pixi.js';
import { Spine } from 'pixi-spine';
import json from '../../assets/json/xj.json';

onMounted(() => {
    const app = new PIXI.Application({ background: '#1099bb', resizeTo: window });
    // await app.init({ background: '#1099bb', resizeTo: window });
    document.getElementById('pixi-skeleton-container').appendChild(app.view);
    // 'http://localhost:5173/src/assets/json/xj.json'
    PIXI.Assets.load('src/assets/json/xj.json').then((resource) => {
        console.log(1111, resource);

        const skeletonData = resource.spineData;
        const skeleton = new Spine(skeletonData);
        console.log(222, skeleton);
        // 设置骨骼动画的位置等属性
        skeleton.x = app.screen.width / 2;
        skeleton.y = app.screen.height;
        skeleton.width = 480;
        skeleton.height = 660;
        app.stage.addChild(skeleton);
        // 播放骨骼动画的频率
        skeleton.state.timeScale = 0.01;
        // 播放骨骼动画
        skeleton.state.setAnimation(0, 'chuxian', true);
        // 开始渲染动画
        app.ticker.add(() => {
            skeleton.update(app.ticker.deltaTime);
        });
        // update yourself
        // skeleton.autoUpdate = true;
    });
})




</script>

<template>
    <div id="pixi-skeleton-container"></div>
</template>

<style scoped></style>
