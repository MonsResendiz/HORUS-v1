<template>
  <div>
    <!-- Menú -->
    <nav class="flex gap-4 bg-gray-800 p-4 text-white">
     <!--  <button @click="current = 'Home'" :class="btnClass('Home')">Inicio</button> -->

    </nav>

    <!-- Contenido dinámico -->
    <component :is="currentComponent" />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import Home from './views/home.vue'
import About from './views/Dashboard.vue'

const current = ref('Home')

const currentComponent = computed(() => {
  if (current.value === 'About') return About
  return Home
})

const btnClass = (tab) => 
  current.value === tab 
    ? 'font-bold underline' 
    : 'hover:underline'
</script>
