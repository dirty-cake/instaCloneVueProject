<template>
  <div class="sign-in">
		<img alt="inst logo" src="../assets/instagramLogo.svg" class="instagram-logo-image">
    <Input type="text" placeholder="Put your login" v-model="userName" />
    <Input type="text" placeholder="Put your password" v-model="password" />
  </div>
    
</template>

<script>
import Input from '../components/Input'
import { ref } from '@vue/composition-api'

export default {
  name: 'SignIn',
  components: {
    Input
  },
  props: {}, 
  setup() {
    const userName = ref('')
    const password = ref('')
    const login = () => {
      console.log(userName, password)
    }
    return {
      userName,
      password,
      login
    }
  }
}
</script>

<style scoped>
.instagram-logo-image {
  height: 51px;
  width: 175px;
}
</style>
