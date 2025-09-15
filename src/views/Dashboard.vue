<template>
  <div class="dashboard">
    <header class="header-dashboard">
      <h1 class="header-dashboard h1">SERVICIOS PUBLICOS</h1>
      <div class="header-dashboard p">
        <span class="name-fis">FISCAL</span>
      </div>
    </header>

    <!-- Cuadros -->
    <div class="secciones">
      <div
        v-for="(item, index) in services"
        :key="index"
        class="seccion">
        <div class="text-dash">{{ item.icon }}</div>
        <h2 class="text-dash">{{ item.title }}</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  { title: "CONSULTAS" },
  { title: " OFICIALES" },
  { title: "PETICIONES" },
  { title: "DELIGENCIAS" },
  { title: "TELEFONIA" }
 
]
</script>
