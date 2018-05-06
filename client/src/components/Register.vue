<template>
  <div>
      <h1>Register</h1>
      <input type="text" name="email" placeholder="email" v-model="email">
      <br>
      <input type="password" name="password" placeholder="password" v-model="password">
      <br>
      <button @click="register">Register</button>
  </div>
</template>
<script>
import AuthenticationService from '@/services/AuthenticationService'

export default {
  data() {
    return {
      email: '',
      password: ''
    };
  },
  watch: {
    email(value) {
      console.log("email: ", value);
    }
  },
  methods:{
      register() {
          console.log('registerd: ', this.email, this.password);
      }
  },
  mounted() {
    setTimeout(() => {
      this.email = "vanxuanbinhan@gmail.com";
    }, 2000);
  }
};
</script>
