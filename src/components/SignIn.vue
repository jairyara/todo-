<template>
  <h1>{{ title }}</h1>
  <form class="form form-signIn">
    <label class="label" for="user">usuario</label>
    <input class="input" name="user" id="user" type="text" required>
    <label class="label" for="password">Contraseña</label>
    <input class="input" id="password" name="password" type="password" required>
    <button class="btn btn-primary" type="submit">ingresar</button>
  </form>
  <router-link to="#">¿Olvidaste la contraseña?</router-link>
</template>

<script>

export default {
  name: 'SignIn',
  props: {
    title: String
  }
}
</script>

<style scoped lang="scss">
h1 {
  margin: 50px 0;
  color: #0054FE;
}

a {
  font-size: 14px;
  color: #0054FE;
}

</style>
