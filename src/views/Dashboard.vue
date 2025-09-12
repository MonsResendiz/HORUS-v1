<template>
   <div class="Dashboard">
     <h1>"Nombre del fiscal"</h1>
     <h2>
        <button class="dash" type="button" @click="secciones = !secciones" ></button>
      </h2>
      <div v-if="secciones">
        <!-- Contenido aquí -->
      </div>     
   </div>
</template>

<script>
export default {
  data() {
    return {
      secciones: false
    }
  }
}
</script>