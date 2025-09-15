<template>
  <div class="registro">
    <h1>Crear Cuenta</h1>

    <form @submit.prevent="registrar">
      <div class="mb-4">
        <label for="nombre">Nombre</label>
        <input v-model="nombre" id="nombre" type="text" required />
      </div>

      <div class="mb-4">
        <label for="email">Correo electrónico</label>
        <input v-model="email" id="email" type="email" required />
      </div>

      <div class="mb-4">
        <label for="password">Contraseña</label>
        <input v-model="password" id="password" type="password" required />
      </div>

      <button type="submit">Registrarse</button>
    </form>

    <div v-if="mensaje" class="message">{{ mensaje }}</div>
    <button @click="$emit('changePage', 'Home')">⬅ Volver</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const nombre = ref('')
const email = ref('')
const password = ref('')
const mensaje = ref('')

function registrar() {
  mensaje.value = `¡Registro exitoso, ${nombre.value}!`
  nombre.value = ''
  email.value = ''
  password.value = ''
}
</script>
