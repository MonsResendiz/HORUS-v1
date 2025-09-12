<template>
  <link rel="stylesheet" href="../assets/home.css" />

  <div class="home">
    <form class="h1">
      <h1>BIENVENIDO A HORUS!</h1>
      <!-- RESGISTRO-->
      <h2>
        <button class="h2-registro" type="button" @click="mostrarRegistro = !mostrarRegistro">
          Registro
        </button>
      </h2>
      <div v-if="mostrarRegistro">
        <div class="mb-4">
          <label class="datos" for="nombreRegistro">Nombre</label>
          <input v-model="nombreRegistro" id="nombreRegistro" type="text" class="relleno-home" required />
        </div>
        <div class="mb-4">
          <label class="datos" for="emailRegistro">Correo electrónico</label>
          <input v-model="emailRegistro" id="emailRegistro" type="email" class="relleno-home" required />
        </div>
        <div class="mb-6">
          <label class="datos" for="passwordRegistro">Contraseña</label>
          <input v-model="passwordRegistro" id="passwordRegistro" type="password" class="relleno-home" required />
        </div>
        <button type="submit" class="buttom-home" @click.prevent="registrar">
          Registrarse
        </button>
        <div v-if="mensajeRegistro" class="message">{{ mensajeRegistro }}</div>
      </div>

      <!-- LOGIN -->
      <h2>
        <button class="h2-login" type="button" @click="mostrarLogin = !mostrarLogin">
          Iniciar Sesión
        </button>
      </h2>
      <div v-if="mostrarLogin">
        <div class="mb-4">
          <label class="datos" for="emailLogin">Correo electrónico</label>
          <input v-model="emailLogin" id="emailLogin" type="email" class="relleno-home" required />
        </div>
        <div class="mb-6">
          <label class="datos" for="passwordLogin">Contraseña</label>
          <input v-model="passwordLogin" id="passwordLogin" type="password" class="relleno-home" required />
        </div>
        <button type="submit" class="buttom-home" @click.prevent="iniciarSesion">
          Entrar
        </button>
        <div v-if="mensajeLogin" class="message">{{ mensajeLogin }}</div>
      </div>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Registro
const nombreRegistro = ref('')
const emailRegistro = ref('')
const passwordRegistro = ref('')
const mensajeRegistro = ref('')
const mostrarRegistro = ref(false)

// Login
const emailLogin = ref('')
const passwordLogin = ref('')
const mensajeLogin = ref('')
const mostrarLogin = ref(false)

function registrar() {
  mensajeRegistro.value = `¡Registro exitoso, ${nombreRegistro.value}!`
  nombreRegistro.value = ''
  emailRegistro.value = ''
  passwordRegistro.value = ''
}

function iniciarSesion() {
  // Aquí puedes agregar la lógica real de autenticación
  mensajeLogin.value = `¡Bienvenido de nuevo, ${emailLogin.value}!`
  emailLogin.value = ''
  passwordLogin.value = ''
}
</script> 
