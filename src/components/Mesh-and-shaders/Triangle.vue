<script setup lang="js">
import { onMounted } from 'vue';
import * as PIXI from 'pixi.js';

onMounted(() => {


    const app = new PIXI.Application({ resizeTo: window });

    document.getElementById('pixi-Triangle-container').appendChild(app.view);

    const geometry = new PIXI.Geometry().addAttribute('aVertexPosition', [-100, -50, 100, -50, 0, 100]);

    const shader = PIXI.Shader.from(
        `
    
        precision mediump float;
        attribute vec2 aVertexPosition;
    
        uniform mat3 translationMatrix;
        uniform mat3 projectionMatrix;
    
        void main() {
            gl_Position = vec4((projectionMatrix * translationMatrix * vec3(aVertexPosition, 1.0)).xy, 0.0, 1.0);
        }`,

        `precision mediump float;
    
        void main() {
            gl_FragColor = vec4(1.0, 0.0, 0.0, 1.0);
        }
    
    `,
    );

    const triangle = new PIXI.Mesh(geometry, shader);

    triangle.position.set(400, 300);

    app.stage.addChild(triangle);

    app.ticker.add((delta) => {
        triangle.rotation += 0.01;
    });
})


</script>

<template>
    <div id="pixi-Triangle-container"></div>
</template>

<style scoped></style>
