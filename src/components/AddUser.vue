<template>
    <form class="add-user">
      <h2>Agregar nuevo usuario</h2>
      <div class="add-user__container">
        <div class="add-user__container--element">
          <label class="label" for="name">nombres</label>
          <input class="input" name="name" id="name" type="text" required>
        </div>
        <div class="add-user__container--element">
          <label class="label" for="user">usuario</label>
          <input class="input" name="user" id="user" type="text" required>
        </div>
        <div class="add-user__container--element">
          <label class="label" for="email">email</label>
          <input class="input" name="email" id="email" type="email" required>
        </div>
        <div class="add-user__container--element">
          <label class="label" for="street">calle</label>
          <input class="input" name="street" id="street" type="text" required>
        </div>
        
        <div class="add-user__container--element">
          <label class="label" for="suite">suite</label>
          <input class="input" name="suite" id="suite" type="text" required>
        </div>
        
        <div class="add-user__container--element">
          <label class="label" for="city">ciudad</label>
          <input class="input" name="city" id="city" type="text" required>
        </div>
        <div class="add-user__container--element">
          <label class="label" for="company">compañía</label>
          <input class="input" id="company" name="company" type="text" required>
        </div>
      </div>
      <button class="btn btn-primary" type="submit" >guardar</button>
    </form>
</template>

<script>
export default {
    name: 'AddUser'
}
</script>

<style lang="scss" scoped>

.add-user {
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
  margin-bottom: 40px;

  &__container {
    margin: 40px 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, calc(50% - 40px));
    gap: 40px;

    &--element {
      input {
        margin-top: 20px;
      }
    }
  }
}

</style>>
