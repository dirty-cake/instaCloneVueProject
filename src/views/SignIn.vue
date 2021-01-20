<template>
<div class="sing-in-view">
  <div class="sign-in">
    <div class="sign-in-content">
      <img alt="inst logo" src="../assets/instagramLogo.svg" class="sing-in-image">
      <Input type="text" placeholder="Put your login" :modelValue="userName" @update:modelValue="value => userName = value" />
      <Input type="password" placeholder="Put your password" v-model="password" />
      <Button :disabled="!userName || !password" @click="login">Sign in </Button>
    </div>

    <div class="sign-in-password">Forgot a password?</div>
  </div>

  <div class="sign-up-block">Don't you have an account? Sign in</div>
  <div class="sign-in-install-app">
    <p>Install the application</p>
    <div class="sign-in-install-app-images">
      <img alt="apple store" src="../assets/appstore.png" class="sing-in-image" />
      <img alt="google store" src="../assets/google-play.png" class="sing-in-image" />
    </div>
  </div>
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
      console.log(userName.value, password.value)
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
.sing-in-view {
  display: inline-block;
  & > :not(:last-child) {
    margin-bottom: 30px;
  }
}
.sign-in {
  border: 2px solid #dbdbdb;
  padding: 30px 45px;
  text-align: center;
}
.sign-in-content {
  border-bottom: 1px solid #dbdbdb;
  margin-bottom: 35px;
  & > :last-child {
    margin-bottom: 25px;
  }
  & > :not(:last-child) {
    margin-bottom: 15px;
  }
}
.sing-in-image {
  height: 40px;
  width: 140px;
  cursor: pointer;
}
.sign-in-password {
  color: rgba(var(--fe0,0,55,107),1);
  font-size: 16px;
  line-height: 14px;
  cursor: pointer;
}
.sign-up-block {
  padding: 25px 15px;
  border: 2px solid #dbdbdb;
  text-align: center;
}
.sign-in-install-app {
  display: flex;
  flex-direction: column;
  text-align: center;
}
.sign-in-install-app-images {
  display: flex;
  justify-content: space-between;
}
</style>
