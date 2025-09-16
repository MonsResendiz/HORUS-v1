<!-- filepath: c:\Users\monse\Documents\HORUS\Horus\src\views\home.vue -->
<template>
  <div class="home">
    <form class="h1">
      <h1>BIENVENIDO A HORUS!</h1>

      <h2>
        <button class="h2-registro" type="button" @click="$emit('changePage', 'Registro')">
          Registro
        </button>
      </h2>

      <h2>
        <button class="h2-login" type="button" @click="$emit('changePage', 'Login')">
          Iniciar Sesión
        </button>
      </h2>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>