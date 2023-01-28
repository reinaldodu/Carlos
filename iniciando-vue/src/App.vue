<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

let nuevavariable = "hola mundo";
let activar=ref(true);
const contador=ref(0);

function cambia() {
  activar.value = !activar.value;
}

console.log(contador.value);

</script>

<template>
  <div>
    <p>{{ nuevavariable.toUpperCase() }}</p>
    <button @click="cambia">{{ activar ? 'Desactivar':'Activar' }}</button>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
