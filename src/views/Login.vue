<template>
<body>
  <div class="login-container">

    <h1><b>Hello Again!</b></h1><br>

    <h2>LOGIN</h2>

    <form  @submit.prevent="login">

    
    <input type="text" id="username" name="username" v-model="username" @input="validateUsername" placeholder ="Enter name" ><br>
    <span v-if="usernameError" class="message">{{ usernameError }}</span><br> 

    
    <input type="number" id="password" name="password" v-model="password" @input="validatePassword" placeholder ="Enter password"><br>
    <span v-if="passwordError" class="message">{{ passwordError }}</span><br>

    <button type="submit">Sign in</button><br>
    <span v-if="merror" class="message">{{ merror }}</span> 

   </form>
  </div>
  </body>
</template>

<script>

export default {
  data() {
    return {
      username: '',
      password: '',
      usernameError: '',
      passwordError: '',
      merror: ''
    };
  },

 methods: {

  validateUsername(){
    const regex = /^[a-zA-Z]+$/;

    if (!regex.test(this.username)){
      console.log("wrong")
      this.usernameError = 'Use alphabets only..!';
      this.username ='';
    } else {
      console.log("yes")
      this.usernameError = '';
    }
  },

  validatePassword(){
    const regex = /^[0-9]+$/;

    if(!regex.test(this.password)){
      this.passwordError = 'use numbers only..!';
      this.passsword = '';
    } else {
      this.passwordError = '';
    }
  },


    async login() {
        if (this.username === "Admin" && this.password === 11) {
            console.log('logged in..!')
            this.$router.push('/HomeView');
        } else if (this.username === '' || this.password === '') {
           console.log('enter login credentials')
            this.merror = 'Enter login credentials..!';
        } else {
          console.log('invalid')
            this.merror = 'Invalid username or password..!';
        }
    }
 }
};
    
</script>


<style scoped>



.login-container {
  font-family: 'Quicksand', sans-serif;
  text-align: center;
  margin: 0;
  padding: 0;
  color: #333;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

body {
  text-align: center;
  margin: 0;
  padding: 0;
}

form {
  background-color: rgba(102, 0, 51, 0.5);
  margin: 20px auto;
  max-width: 400px;
  padding: 30px;
  border-radius: 5px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
}

h1 {
  font-family: 'Roboto Mono', monospace;
  text-align: center;
  color: #333333;
}

h2 {
  font-family: 'Gill Sans', sans-serif;
  text-align: center;
  color: #333333;
}

label {
  font-family: 'Gill Sans', sans-serif;
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

input {
  margin: 10px 0;
  width: 80%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

.message {
  font-family: 'Roboto Mono', monospace;
  color: #ac0707;
}

p{
 color: #333;   
}

button {
  background-color: #660033;
  color: #ffffff;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  width: 50%;
}


</style>
