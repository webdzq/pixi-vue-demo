<script setup lang="js">
import { onMounted } from 'vue';
import * as PIXI from 'pixi.js';

onMounted(() => {


  const app = new PIXI.Application({ background: '#1099bb', resizeTo: window });

  document.getElementById('pixi-Click-container').appendChild(app.view);

  // Scale mode for all textures, will retain pixelation
  PIXI.settings.SCALE_MODE = PIXI.SCALE_MODES.NEAREST;

  const sprite = PIXI.Sprite.from('https://pixijs.com/assets/bunny.png');

  // Set the initial position
  sprite.anchor.set(0.5);
  sprite.x = app.screen.width / 2;
  sprite.y = app.screen.height / 2;

  // Opt-in to interactivity
  sprite.eventMode = 'static';

  // Shows hand cursor
  sprite.cursor = 'pointer';

  // Pointers normalize touch and mouse (good for mobile and desktop)
  sprite.on('pointerdown', onClick);

  // Alternatively, use the mouse & touch events:
  // sprite.on('click', onClick); // mouse-only
  // sprite.on('tap', onClick); // touch-only

  app.stage.addChild(sprite);

  function onClick() {
    sprite.scale.x *= 1.25;
    sprite.scale.y *= 1.25;
  }
})


</script>

<template>
  <div id="pixi-Click-container"></div>
</template>

<style scoped></style>
