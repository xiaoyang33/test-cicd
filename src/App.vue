

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h3>{{query}}-----</h3>
  <button @click="add">增加</button>
  <!-- <div class="rounded-full  h-10 w-10 shadow-slate-400 bg-orange-400 shadow"></div> -->
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>
<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { ref } from '@vue/reactivity'
import { watchEffect } from '@vue/runtime-core';
import HelloWorld from './components/HelloWorld.vue'
const query = ref(1)

const add = ()=>{
  query.value++
}
const fun = () => {
  console.log(11111);

  console.log(query);
  return query.value + 1
}

watchEffect(()=>{
  fun()
})
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
