<template>
  <div>
    <SignIn />
    <!-- <SignUp /> -->
  </div>
</template>

<script>
import SignIn from './views/SignIn'
// import SignUp from './views/SignUp'

export default {
  name: 'App',
  components: {
    SignIn, 
    // SignUp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}
</style>
