<template>
  <div class="home">
    <SignIn title="Iniciar sesión"/>
  </div>
</template>

<script>
import SignIn from '@/components/SignIn.vue'

export default {
  name: 'HomeView',
  components: {
    SignIn
  }
}
</script>
