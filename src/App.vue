<template>
  <SignIn />
</template>

<script>
import SignIn from './views/SignIn'

export default {
  name: 'App',
  components: {
    SignIn
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* background-color: #fafafa; */
  height: 100%;
}
</style>
