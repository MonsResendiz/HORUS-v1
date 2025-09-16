<template>
  <div class="dashboard">
    <!-- Contenedor de Servicios Públicos + Fiscal -->
    <div class="servicios-container">
      <!-- Servicios Públicos -->
      <div class="servicio-publico">
        <h1>SERVICIOS PUBLICOS</h1>
      </div>

      <!-- Fiscal centrado -->
      <div class="name-fis">
        FISCAL
      </div>
    </div>

    <!-- Cuadros -->
    <div class="secciones">
      <div
        v-for="(item, index) in services"
        :key="index"
        class="seccion">
        <h2 class="text-dash">{{ item.title }}</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  { title: "CONSULTAS" },
  { title: "OFICIALES" },
  { title: "PETICIONES" },
  { title: "DELIGENCIAS" },
  { title: "TELEFONIA" }
]
</script>
