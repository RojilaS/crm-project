<template>
  <div class="login-container">
    <h1>LOGIN PAGE</h1>
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" v-model="username" required><br/>

    <label for="password">Password:</label>
    <input type="number" id="password" name="password" v-model="password"><br>

    <button @click="login()">LOGIN</button><br><br>

    
  </div>
</template>

<script>

export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },

  methods: {
    async login() {
      if (this.username === '' || this.password === '') {
        alert('Enter essential details');
      } else {
        this.$router.push('/HomeView');

      }
    }
  }
};
</script>

<style scoped>
  .login-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh; 
    background-color: #f4f4f4;
    padding: 20px; 
  }

  .login-form {
    max-width: 300px;
    padding: 20px;
    background-color: #ffffff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
  }

  h2 {
    text-align: center;
    color: #333333;
  }

  label {
    display: block;
    margin: 10px 0;
    color: #555555;
  }

  input {
    width: 100%;
    padding: 8px;
    margin-bottom: 15px;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-radius: 4px;
  }

  button {
    background-color: #4caf50;
    color: #ffffff;
    padding: 10px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    width: 100%;
  }

  button:hover {
    background-color: #45a049;
  }
</style>
