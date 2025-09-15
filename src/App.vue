<template>
  <div>
    <component 
      :is="currentComponent" 
      @changePage="current = $event" 
    />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

import Home from './views/home.vue'
import Registro from './views/registro.vue'
import Login from './views/login.vue'
import Dashboard from './views/Dashboard.vue'

const current = ref('Home')

const currentComponent = computed(() => {
  if (current.value === 'Dashboard') return Dashboard
  if (current.value === 'Registro') return Registro
  if (current.value === 'Login') return Login
  return Home
})
</script>
