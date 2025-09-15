<template>
  <div class="login">
    <h1>Iniciar Sesión</h1>

    <form @submit.prevent="iniciarSesion">
      <div class="mb-4">
        <label for="email">Correo electrónico</label>
        <input v-model="email" id="email" type="email" required />
      </div>

      <div class="mb-4">
        <label for="password">Contraseña</label>
        <input v-model="password" id="password" type="password" required />
      </div>

      <button type="submit">Entrar</button>
    </form>

    <div v-if="mensaje" class="message">{{ mensaje }}</div>
    <button @click="$emit('changePage', 'Home')">⬅ Volver</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const mensaje = ref('')

function iniciarSesion() {
  mensaje.value = `¡Bienvenido de nuevo, ${email.value}!`
  email.value = ''
  password.value = ''

  setTimeout(() => {
    mensaje.value = 'Has iniciado sesión correctamente.'
    emit('changePage', 'Dashboard')
  }, 1000)

const emit = defineEmits(['changePage'])
}
</script>
