<template>
  <router-view/>
</template>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  scroll-behavior: smooth;
  background-color: #F5F6FA;
}

#app {
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #121212;
}


.label {
  text-transform: capitalize;
}

.input {
  padding: 5px 10px;
  width: 100%;
  height: 35px;
  border: 1px solid #0054FE;
  border-radius: 4px;
}

.form {
  padding: 20px;
  width: 100%;
  height: 100%;
  max-width: 900px;
  margin: 0 auto;
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  flex-direction: column;

  &-signIn {
    min-height: 40vh;
  }

  .btn {
    margin: 0 auto;
  }
}

.btn {
  width: 200px;
  height: 40px;
  text-transform: capitalize;
  font-size: 18px;
  cursor: pointer;
  border-radius: 8px;

  &-primary {
    background-color: #0054FE;
    color: white;
    border: none;
  }

  &-secondary {
    background-color: transparent;
    border: 2px solid #0054FE;
    color: #0054FE;
  }
}

.dashboard {
    width: 100%;
    height: 100vh;
    display: grid;
    grid-template-areas: 'aside header' 'aside content';
    grid-template-columns: 250px 1fr;
    grid-template-rows: 90px 1fr;
    gap: 40px;
    
    &__header {
        width: calc(100% - 40px);
        height: 100%;
        background-color: white;
    }
    
    &__content {
        grid-area: content;
        width: calc(100% - 40px);
        height: calc(100% - 40px);
        padding: 30px;
        overflow: scroll;
        background-color: white;
    }
}

</style>
