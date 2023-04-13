<template>
  <div>
    <h1>Register</h1>
    <input type="text" name="email" placeholder="email" v-model="email" />
    <input
      type="text"
      name="password"
      placeholder="password"
      v-model="password"
    />
    <button @click="register">submit</button>
  </div>
</template>

<script>
import AuthenticationService from "../services/AuthenticationService";
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },

  methods: {
    async register() {
      const response = await AuthenticationService.register({
        email: this.email,
        password: this.password,
      });
      console.log * ("response", response);
    },
  },
};
</script>

<style scoped></style>
