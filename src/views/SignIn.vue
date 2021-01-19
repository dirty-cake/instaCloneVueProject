<template>
  <div class="sign-in">
		<img alt="inst logo" src="../assets/instagramLogo.svg" class="instagram-logo-image">
    <Input type="text" placeholder="Put your login" v-model="userName" />
    <Input type="text" placeholder="Put your password" v-model="password" />
    <Button :onClick="login">Sign in </Button>
  </div>
    
</template>

<script>
import Input from '../components/Input'
import Button from '../components/Button'
import { ref } from 'vue'

export default {
  name: 'SignIn',
  components: {
    Input, 
    Button
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

<style lang="scss" scoped>
.sign-in {
  &:not(:last-child) {
    margin-bottom: 15px;
  }
}

.instagram-logo-image {
  height: 51px;
  width: 175px;
}
</style>
