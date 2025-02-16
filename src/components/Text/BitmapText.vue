<script setup lang="js">
import { onMounted } from 'vue';
import * as PIXI from 'pixi.js';

onMounted(() => {
  const app = new PIXI.Application({ background: '#1099bb', resizeTo: window });

  document.getElementById('pixi-BitmapText-container').appendChild(app.view);

  PIXI.Assets.load('https://pixijs.com/assets/bitmap-font/desyrel.xml').then(() => {
    const bitmapFontText = new PIXI.BitmapText('bitmap fonts are supported!\nWoo yay!', {
      fontName: 'Desyrel',
      fontSize: 55,
      align: 'left',
    });

    bitmapFontText.x = 50;
    bitmapFontText.y = 200;

    app.stage.addChild(bitmapFontText);
  });
})

</script>

<template>
  <div id="pixi-BitmapText-container"></div>
</template>

<style scoped></style>
