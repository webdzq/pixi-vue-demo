<script setup lang="js">
import { onMounted } from 'vue';
import * as PIXI from 'pixi.js';

onMounted(() => {


  const app = new PIXI.Application({ background: '#1099bb', resizeTo: window });

  document.getElementById('pixi-Promise-container').appendChild(app.view);

  // Start loading right away and create a promise
  const texturePromise = PIXI.Assets.load('https://pixijs.com/assets/bunny.png');

  // When the promise resolves, we have the texture!
  texturePromise.then((resolvedTexture) => {
    // create a new Sprite from the resolved loaded Texture
    const bunny = PIXI.Sprite.from(resolvedTexture);

    // center the sprite's anchor point
    bunny.anchor.set(0.5);

    // move the sprite to the center of the screen
    bunny.x = app.screen.width / 2;
    bunny.y = app.screen.height / 2;

    app.stage.addChild(bunny);
  });
})


</script>

<template>
  <div id="pixi-Promise-container"></div>
</template>

<style scoped></style>
