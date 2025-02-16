<template>
  <div class="left-menu">
    <!-- 这里可以添加具体的菜单选项，比如以下示例 -->
    <ul @click="itemUpAndDownClick">
      <li>
        <span class="item-click">+Basic </span>
        <ul class="item-children" style="">
          <li class="item" @click="itemClick('Container',$event)">Container</li>
          <li class="item" @click="itemClick('Skeleton',$event)">Skeleton</li>
          <li class="item" @click="itemClick('TransparentBackground',$event)">TransparentBackground</li>
          <li class="item" @click="itemClick('Tinting',$event)">Tinting</li>
          <li class="item" @click="itemClick('CacheAsBitmap',$event)">CacheAsBitmap</li>
          <li class="item" @click="itemClick('ParticleContainer',$event)">ParticleContainer</li>
          <li class="item" @click="itemClick('BlendModes',$event)">BlendModes</li>
          <li class="item" @click="itemClick('SimplePlane',$event)">SimplePlane</li>
        </ul>
      </li>
      <li>
        <span class="item-click">+Advanced </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Slots',$event)">Slots</li>
          <li class="item" @click="itemClick('ScratchCard',$event)">ScratchCard</li>
          <li class="item" @click="itemClick('StarWarp',$event)">StarWarp</li>
          <li class="item" @click="itemClick('MouseTrail',$event)">MouseTrail</li>
          <li class="item" @click="itemClick('ScreenShot',$event)">ScreenShot</li>
          <li class="item" @click="itemClick('CollisionDetection',$event)">CollisionDetection</li>
          <li class="item" @click="itemClick('Spinners',$event)">Spinners</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Sprite </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Basic',$event)">Basic</li>
          <li class="item" @click="itemClick('TextureSwap',$event)">TextureSwap</li>
          <li class="item" @click="itemClick('AnimatedSpriteExplosion',$event)">AnimatedSpriteExplosion</li>
          <li class="item" @click="itemClick('AnimatedSpriteJet',$event)">AnimatedSpriteJet</li>
          <li class="item" @click="itemClick('AnimatedSpriteAnimationSpeed',$event)">AnimatedSpriteAnimationSpeed</li>
          <li class="item" @click="itemClick('TilingSprite',$event)">TilingSprite</li>
          <li class="item" @click="itemClick('Video',$event)">Video</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Text </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('PixiText',$event)">PixiText</li>
          <li class="item" @click="itemClick('BitmapText',$event)">BitmapText</li>
          <li class="item" @click="itemClick('FromFont',$event)">FromFont</li>
          <li class="item" @click="itemClick('WebFont',$event)">WebFont</li>
        </ul>
      </li>
      <li>
        <span class="item-click">+Graphics </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Simple',$event)">Simple</li>
          <li class="item" @click="itemClick('Advanced',$event)">Advanced</li>
          <li class="item" @click="itemClick('Dynamic',$event)">Dynamic</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Events </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Click',$event)">Click</li>
          <li class="item" @click="itemClick('Interactivity',$event)">Interactivity</li>
          <li class="item" @click="itemClick('Dragging',$event)">Dragging</li>
          <li class="item" @click="itemClick('CustomMouseIcon',$event)">CustomMouseIcon</li>
          <li class="item" @click="itemClick('CustomHitarea',$event)">CustomHitarea</li>
          <li class="item" @click="itemClick('Logger',$event)">Logger</li>
          <li class="item" @click="itemClick('NestedBoundaryWithProjection',$event)">NestedBoundaryWithProjection</li>
          <li class="item" @click="itemClick('PointerTracker',$event)">PointerTracker</li>
          <li class="item" @click="itemClick('Slider',$event)">Slider</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Masks </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Graphics',$event)">Graphics</li>
          <li class="item" @click="itemClick('Sprite',$event)">Sprite</li>
          <li class="item" @click="itemClick('Filter',$event)">Filter</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Filters-basic </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Blur',$event)">Blur</li>
          <li class="item" @click="itemClick('ColorMatrix',$event)">ColorMatrix</li>
          <li class="item" @click="itemClick('DisplacementMapCrawlies',$event)">DisplacementMapCrawlies</li>
          <li class="item" @click="itemClick('DisplacementMapFlag',$event)">DisplacementMapFlag</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Filters-advanced </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('MouseBlending',$event)">MouseBlending</li>
          <li class="item" @click="itemClick('Custom',$event)">Custom</li>
          <li class="item" @click="itemClick('ShaderToyFilterRenderTexture',$event)">ShaderToyFilterRenderTexture</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Mesh-and-shaders </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('TexturedMeshBasic',$event)">TexturedMeshBasic</li>
          <li class="item" @click="itemClick('TexturedMeshAdvanced')">TexturedMeshAdvanced</li>
          <li class="item" @click="itemClick('Triangle')">Triangle</li>
          <li class="item" @click="itemClick('TriangleColor')">TriangleColor</li>
          <li class="item" @click="itemClick('TriangleTextured')">TriangleTextured</li>
          <li class="item" @click="itemClick('Uniforms')">Uniforms</li>
          <li class="item" @click="itemClick('SharingGeometry')">SharingGeometry</li>
          <li class="item" @click="itemClick('SharedShader')">SharedShader</li>
          <li class="item" @click="itemClick('MergingGeometry')">MergingGeometry</li>
          <li class="item" @click="itemClick('InterleavingGeometry')">InterleavingGeometry</li>
          <li class="item" @click="itemClick('InstancedGeometry')">InstancedGeometry</li>
          <li class="item" @click="itemClick('ShaderToyMesh')">ShaderToyMesh</li>
          <li class="item" @click="itemClick('MultiPassShaderGeneratedMesh')">MultiPassShaderGeneratedMesh</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Texture </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('TextureRotate',$event)">TextureRotate</li>
          <li class="item" @click="itemClick('RenderTextureBasic',$event)">RenderTextureBasic</li>
          <li class="item" @click="itemClick('RenderTextureAdvanced',$event)">RenderTextureAdvanced</li>
          <li class="item" @click="itemClick('GradientBasic',$event)">GradientBasic</li>
          <li class="item" @click="itemClick('GradientResource',$event)">GradientResource</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Assets </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Promise',$event)">Promise</li>
          <li class="item" @click="itemClick('Async',$event)">Async</li>
          <li class="item" @click="itemClick('Multiple',$event)">Multiple</li>
          <li class="item" @click="itemClick('Background',$event)">Background</li>
          <li class="item" @click="itemClick('Bundle',$event)">Bundle</li>
        </ul>
      </li>
      <li >
        <span class="item-click">+Offscreen-canvas </span>
        <ul class="item-children">
          <li class="item" @click="itemClick('Basico',$event)">Basico</li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script setup>
// 这里可以添加与菜单相关的逻辑，比如菜单点击事件等，暂时先为空
import { ref, defineEmits } from 'vue';


const emits = defineEmits(['left-menu-params']);
const itemClick = (param,event) => {
  console.log('left-menu-params--',event, param)
  emits('left-menu-params', param);
}
const itemUpAndDownClick = (evt) => {
  // isUpAndDown.value=!isUpAndDown.value
  console.log('evt-', evt.target)
  const domObj = evt.target
  if (domObj.classList.contains('item-click')) {
    const xdDomObj = domObj.parentNode.querySelector('ul')
    console.log('xdDomObj', xdDomObj.style.display)
    const isShow = xdDomObj.style.display === 'none'
    if (isShow) {
      xdDomObj.style.display = 'block'
    } else {
      xdDomObj.style.display = 'none'
    }

  }
}
</script>

<style scoped>
.left-menu {
  width: 300px;
  background-color: #e6f1e2;
  height: 100vh;
  position: fixed;
  left: 0;
  top: 5vh;
  text-align: left;
  overflow-y: scroll;
}

.left-menu ul {
  list-style-type: none;
  padding: 0;
}

.left-menu li {
  padding: 10px;
  cursor: pointer;
  
}

.left-menu li:hover {
  background-color: #e0e0e0;
}

.item{
  background-color: #d7ea97;
 
}
.item-click{
  display: inline-block;
  width:100%;
}

.item-children{
  display: none;
}

</style>