<template>
  <div class="home">
    <form class="h1">
      <h1>BIENVENIDO A HORUS!</h1>

      <h2>
        <RouterLink class="h2-registro" to="/registro">Registro</RouterLink>
      </h2>

      <h2>
        <RouterLink class="h2-login" to="/login">Iniciar Sesión</RouterLink>
      </h2>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>