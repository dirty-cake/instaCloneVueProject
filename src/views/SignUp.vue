<template>
<div class="sing-up-view">
  <div class="sign-up">
    <div class="sign-up-header">
			<img alt="inst logo" src="../assets/instagramLogo.svg" class="sing-up-image">
      <p>Sign up to follow your friends' photos and videos</p>
    </div>
    <div class="sign-up-content">
      <Input type="text" placeholder="Put your email" v-model="email"/>
      <Input type="text" placeholder="Put your name and surname" v-model="fullName"/>
      <Input type="text" placeholder="Put your nickname" v-model="nickname"/>
      <Input type="password" placeholder="Put your password" v-model="password"/>
			<Button :disabled="!email || !fullName || !nickname || !password" @click="signUp">Sign up</Button>
    </div>
		<div>
			<div>By registering you agree to</div>
			<div>our terms, data policy and cookie policy</div>
		</div>
  </div>
	<div class="sign-in-block">
		Do you have an account? Sign in!
	</div>
</div>
</template>

<script>
import Input from '../components/Input'
import Button from '../components/Button'
import { ref } from 'vue'
export default {
  name: 'SignUp',
  components: {
    Input, 
    Button
  },
  props: {}, 
  setup() {
    const email = ref('')
    const fullName = ref('')
    const nickname = ref('')
    const password = ref('')
    const signUp = () => {
      console.log(email.value, fullName.value, nickname.value, password.value)
    }
    return {
      email,
      fullName,
			nickname,
			password, 
			signUp
    }
  }
}
</script>

<style lang="scss" scoped>
	.sing-up-view {
		display: inline-block;
		& > :not(:last-child) {
			margin-bottom: 30px;
		}
	}
	.sign-up {
		border: 2px solid #dbdbdb;
		padding: 30px 45px;
		text-align: center;
		& > :not(:last-child) {
			margin-bottom: 30px;
		}
	}
	.sign-up-header {
		border-bottom: 1px solid #dbdbdb;
	}
	.sign-up-content {
		border-bottom: 1px solid #dbdbdb;
		margin-bottom: 35px;
		& > :last-child {
			margin-bottom: 25px;
		}
		& > :not(:last-child) {
			margin-bottom: 15px;
		}
	}
	.sing-up-image {
		height: 40px;
		width: 140px;
		cursor: pointer;
	}
	.sign-in-block {
  padding: 25px 15px;
  border: 2px solid #dbdbdb;
  text-align: center;
}
</style>
