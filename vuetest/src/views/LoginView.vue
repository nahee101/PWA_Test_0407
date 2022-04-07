<template>
  <div>
    <h1>This is a login page</h1>
    <input type="text" v-model = "user">
    <input type="password">

    <button @click = "loginUser">Login</button>
    <button @click = " $router.push('/') ">취소</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'LoginView',
  data: () => ({
    user: ''
  }),
  methods: {
    loginUser: function() {
      this.$emit('login-user', this.user);
      this.$router.push('/');
    }
  }
}
</script>

