<template>
  <div class="main-content">
    <Container v-if="currentComponent === 'Container'" />
    <Skeleton v-else-if="currentComponent === 'Skeleton'" />
    <TransparentBackground v-else-if="currentComponent === 'TransparentBackground'" />
    <Tinting v-else-if="currentComponent === 'Tinting'" />
    <CacheAsBitmap v-else-if="currentComponent === 'CacheAsBitmap'" />
    <ParticleContainer v-else-if="currentComponent === 'ParticleContainer'" />
    <BlendModes v-else-if="currentComponent === 'BlendModes'" />
    <SimplePlane v-else-if="currentComponent === 'SimplePlane'" />


    <Slots v-else-if="currentComponent === 'Slots'" />
    <ScratchCard v-else-if="currentComponent === 'ScratchCard'" />
    <StarWarp v-else-if="currentComponent === 'StarWarp'" />
    <MouseTrail v-else-if="currentComponent === 'MouseTrail'" />
    <ScreenShot v-else-if="currentComponent === 'ScreenShot'" />
    <CollisionDetection v-else-if="currentComponent === 'CollisionDetection'" />
    <Spinners v-else-if="currentComponent === 'Spinners'" />

    <Basic v-else-if="currentComponent === 'Basic'" />
    <TextureSwap v-else-if="currentComponent === 'TextureSwap'" />
    <AnimatedSpriteExplosion v-else-if="currentComponent === 'AnimatedSpriteExplosion'" />
    <AnimatedSpriteJet v-else-if="currentComponent === 'AnimatedSpriteJet'" />
    <AnimatedSpriteAnimationSpeed v-else-if="currentComponent === 'AnimatedSpriteAnimationSpeed'" />
    <TilingSprite v-else-if="currentComponent === 'TilingSprite'" />
    <Video v-else-if="currentComponent === 'Video'" />

    <PixiText v-else-if="currentComponent === 'PixiText'" />
    <BitmapText v-else-if="currentComponent === 'BitmapText'" />
    <FromFont v-else-if="currentComponent === 'FromFont'" />
    <WebFont v-else-if="currentComponent === 'WebFont'" />
    
    <Simple v-else-if="currentComponent === 'Simple'" />
    <Advanced v-else-if="currentComponent === 'Advanced'" />
    <Dynamic v-else-if="currentComponent === 'Dynamic'" />

    <Click v-else-if="currentComponent === 'Click'" />
    <Interactivity v-else-if="currentComponent === 'Interactivity'" />
    <Dragging v-else-if="currentComponent === 'Dragging'" />
    <CustomMouseIcon v-else-if="currentComponent === 'CustomMouseIcon'" />
    <CustomHitarea v-else-if="currentComponent === 'CustomHitarea'" />
    <Logger v-else-if="currentComponent === 'Logger'" />
    <NestedBoundaryWithProjection v-else-if="currentComponent === 'NestedBoundaryWithProjection'" />
    <PointerTracker v-else-if="currentComponent === 'PointerTracker'" />
    <Slider v-else-if="currentComponent === 'Slider'" />

    <Graphics v-else-if="currentComponent === 'Graphics'" />
    <Sprite v-else-if="currentComponent === 'Sprite'" />
    <Filter v-else-if="currentComponent === 'Filter'" />

    <Blur v-else-if="currentComponent === 'Blur'" />
    <ColorMatrix v-else-if="currentComponent === 'ColorMatrix'" />
    <DisplacementMapCrawlies v-else-if="currentComponent === 'DisplacementMapCrawlies'" />
    <DisplacementMapFlag v-else-if="currentComponent === 'DisplacementMapFlag'" />
    
    <MouseBlending v-else-if="currentComponent === 'MouseBlending'" />
    <Custom v-else-if="currentComponent === 'Custom'" />
    <ShaderToyFilterRenderTexture v-else-if="currentComponent === 'ShaderToyFilterRenderTexture'" />
    
    <TexturedMeshBasic v-else-if="currentComponent === 'TexturedMeshBasic'" />
    <TexturedMeshAdvanced v-else-if="currentComponent === 'TexturedMeshAdvanced'" />
    <Triangle v-else-if="currentComponent === 'Triangle'" />
    <TriangleColor v-else-if="currentComponent === 'TriangleColor'" />
    <TriangleTextured v-else-if="currentComponent === 'TriangleTextured'" />
    <Uniforms v-else-if="currentComponent === 'Uniforms'" />
    <SharingGeometry v-else-if="currentComponent === 'SharingGeometry'" />
    <SharedShader v-else-if="currentComponent === 'SharedShader'" />
    <MergingGeometry v-else-if="currentComponent === 'MergingGeometry'" />
    <InterleavingGeometry v-else-if="currentComponent === 'InterleavingGeometry'" />
    <InstancedGeometry v-else-if="currentComponent === 'InstancedGeometry'" />
    <ShaderToyMesh v-else-if="currentComponent === 'ShaderToyMesh'" />
    <MultiPassShaderGeneratedMesh v-else-if="currentComponent === 'MultiPassShaderGeneratedMesh'" />
    
    <TextureRotate v-else-if="currentComponent === 'TextureRotate'" />
    <RenderTextureBasic v-else-if="currentComponent === 'RenderTextureBasic'" />
    <RenderTextureAdvanced v-else-if="currentComponent === 'RenderTextureAdvanced'" />
    <GradientBasic v-else-if="currentComponent === 'GradientBasic'" />
    <GradientResource v-else-if="currentComponent === 'GradientResource'" />
   
    <Promise v-else-if="currentComponent === 'Promise'" />
    <Async v-else-if="currentComponent === 'Async'" />
    <Multiple v-else-if="currentComponent === 'Multiple'" />
    <Background v-else-if="currentComponent === 'Background'" />
    <Bundle v-else-if="currentComponent === 'Bundle'" />
    
    <Basico v-else-if="currentComponent === 'Basico'" />


  </div>
</template>

<script setup>
// 这里可以添加与主要内容相关的逻辑，暂时先为空
import { inject, defineProps, ref } from 'vue'

import Container from "./components/Basic/Container.vue";
import Skeleton from "./components/Basic/Skeleton.vue";
import TransparentBackground from "./components/Basic/TransparentBackground.vue";
import Tinting from "./components/Basic/Tinting.vue";
import CacheAsBitmap from "./components/Basic/CacheAsBitmap.vue";
import ParticleContainer from "./components/Basic/ParticleContainer.vue";
import BlendModes from "./components/Basic/BlendModes.vue";
import SimplePlane from "./components/Basic/SimplePlane.vue";

import Slots from "./components/Advanced/Slots.vue";
import ScratchCard from "./components/Advanced/ScratchCard.vue";
import StarWarp from "./components/Advanced/StarWarp.vue";
import MouseTrail from "./components/Advanced/MouseTrail.vue";
import ScreenShot from "./components/Advanced/ScreenShot.vue";
import CollisionDetection from "./components/Advanced/CollisionDetection.vue";
import Spinners from "./components/Advanced/Spinners.vue";

import  Basic  from "./components/Sprite/Basic.vue";
import  TextureSwap  from "./components/Sprite/TextureSwap.vue";
import  AnimatedSpriteExplosion  from "./components/Sprite/AnimatedSpriteExplosion.vue";
import  AnimatedSpriteJet  from "./components/Sprite/AnimatedSpriteJet.vue";
import  AnimatedSpriteAnimationSpeed  from "./components/Sprite/AnimatedSpriteAnimationSpeed.vue";
import  TilingSprite  from "./components/Sprite/TilingSprite.vue";
import  Video  from "./components/Sprite/Video.vue";

import  PixiText  from "./components/Text/PixiText.vue";
import  BitmapText  from "./components/Text/BitmapText.vue";
import  FromFont  from "./components/Text/FromFont.vue";
import  WebFont  from "./components/Text/WebFont.vue";

import  Simple  from "./components/Graphics/Simple.vue";
 import  Advanced  from "./components/Graphics/Advanced.vue";
 import  Dynamic  from "./components/Graphics/Dynamic.vue";

 import  Click  from "./components/Events/Click.vue";
 import  Interactivity  from "./components/Events/Interactivity.vue";
 import  Dragging  from "./components/Events/Dragging.vue";
 import  CustomMouseIcon  from "./components/Events/CustomMouseIcon.vue";
 import  CustomHitarea  from "./components/Events/CustomHitarea.vue";
 import  Logger  from "./components/Events/Logger.vue";
 import  NestedBoundaryWithProjection  from "./components/Events/NestedBoundaryWithProjection.vue";
 import  PointerTracker  from "./components/Events/PointerTracker.vue";
 import  Slider  from "./components/Events/Slider.vue";

 import  Graphics  from "./components/Masks/Graphics.vue";
 import  Sprite  from "./components/Masks/Sprite.vue";
 import  Filter  from "./components/Masks/Filter.vue";


 import  Blur  from "./components/Filters-basic/Blur.vue";
 import  ColorMatrix  from "./components/Filters-basic/ColorMatrix.vue";
 import  DisplacementMapCrawlies  from "./components/Filters-basic/DisplacementMapCrawlies.vue";
 import  DisplacementMapFlag  from "./components/Filters-basic/DisplacementMapFlag.vue";


 import  MouseBlending  from "./components/Filters-advanced/MouseBlending.vue";
 import  Custom  from "./components/Filters-advanced/Custom.vue";
 import  ShaderToyFilterRenderTexture  from "./components/Filters-advanced/ShaderToyFilterRenderTexture.vue";

 import  TexturedMeshBasic  from "./components/Mesh-and-shaders/TexturedMeshBasic.vue";
 import  TexturedMeshAdvanced  from "./components/Mesh-and-shaders/TexturedMeshAdvanced.vue";
 import  Triangle  from "./components/Mesh-and-shaders/Triangle.vue";
 import  TriangleColor  from "./components/Mesh-and-shaders/TriangleColor.vue";
 import  TriangleTextured  from "./components/Mesh-and-shaders/TriangleTextured.vue";
 import  Uniforms  from "./components/Mesh-and-shaders/Uniforms.vue";
 import  SharingGeometry  from "./components/Mesh-and-shaders/SharingGeometry.vue";
 import  SharedShader  from "./components/Mesh-and-shaders/SharedShader.vue";
 import  MergingGeometry  from "./components/Mesh-and-shaders/MergingGeometry.vue";
 import  InterleavingGeometry  from "./components/Mesh-and-shaders/InterleavingGeometry.vue";
 import  InstancedGeometry  from "./components/Mesh-and-shaders/InstancedGeometry.vue";
 import  ShaderToyMesh  from "./components/Mesh-and-shaders/ShaderToyMesh.vue";
 import  MultiPassShaderGeneratedMesh  from "./components/Mesh-and-shaders/MultiPassShaderGeneratedMesh.vue";
 
 import  TextureRotate  from "./components/Texture/TextureRotate.vue";
 import  RenderTextureBasic  from "./components/Texture/RenderTextureBasic.vue";
 import  RenderTextureAdvanced  from "./components/Texture/RenderTextureAdvanced.vue";
 import  GradientBasic  from "./components/Texture/GradientBasic.vue";
 import  GradientResource  from "./components/Texture/GradientResource.vue";

 import  Promise  from "./components/Assets/Promise.vue";
 import  Async  from "./components/Assets/Async.vue";
 import  Multiple from "./components/Assets/Multiple.vue";
 import  Background from "./components/Assets/Background.vue";
 import  Bundle from "./components/Assets/Bundle.vue";

 import  Basico from "./components/Offscreen-canvas/Basic.vue";

const sharedData = ref('')
const currentComponent = ref('Container');
// currentComponent.value = componentName;


const getMenuVal = (msg) => {
  console.log("子组件方法被调用")
  console.log('sharedData', msg)
  sharedData.value = msg
  currentComponent.value = msg;
};
defineExpose({
  getMenuVal
})
</script>

<style scoped>
.main-content {
  margin-left: 200px;
  /* 留出左侧菜单的宽度空间 */
  padding: 20px;
}
</style>