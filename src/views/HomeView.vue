<script setup>
import SquareNoAnimation from '../components/SquareNoAnimation.vue'
</script>

<template>
  <main>
    <div class="container">
      <SquareNoAnimation
        v-for="n in 400"
        :key="n"
        class="square"
        :style="{
          // transform: `scale(${1 - n * 0.1001}) rotate(${n * 4102}deg) translate(${n * 1}px, ${n * 1}px)`,

          // transform: `scale(${1 - n * .2}) rotate(${n * 0}deg) translate(${n * 0}px, ${n * 0}px)`,

          // transform: `scale(${2 - n * 0.003}) rotate(${n * 900}deg) translate(${n * 2}px, ${n * 2}px)`,
          // transform: `scale(${3 - n * 0.0055}) rotate(${n * 2040}deg) translate(${n * 2}px, ${n * 2}px)`,
          transform: `scale(${1 - n * -0.022}) rotate(${n * -1280909}deg) translate(${n * .05}px, ${n * .4}px)`,

          // zIndex: 305 

          zIndex: 305 - n
        }"
      />
    </div>
  </main>
</template>

<style scoped>
.square {
  position: absolute;
  top: 50%;
  left: 50%;
  transform-origin: center;
  padding: 
25px;
  box-shadow:
    0 4px 6px rgba(185, 182, 182, 0.233),
    0 8px 16px rgba(0, 0, 0, 0.15),
    0 12px 24px rgba(0, 0, 0, 0.2);
}

.container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

main {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  /* background-color: #ffffffcc; */
  background-color: rgb(52, 51, 50);
  /* background: linear-gradient(135deg, #dde8f0, #f8ead8, #f5f5f5); */
  font-family: 'IBM Plex Mono';
  color: #333;
}

main::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  opacity: 0.45;
  z-index: -1;
}
</style>
