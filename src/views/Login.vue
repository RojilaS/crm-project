<template>
<body>
  <div class="login-container">
    <h1>LOGIN PAGE</h1>
    <form  @submit.prevent="login">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" v-model="username" @input="validateUsername" required><br/>
    <p v-if="showValidationMessage">{{ validationMessage }}</p>

    <label for="password">Password:</label>
    <input type="number" id="password" name="password" v-model="password" inputmode="numeric"><br><br>

     <button type="submit">LOGIN</button><br>
   </form>
  </div>
  </body>
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
     validateUsername(){
        const alphabet = /^[A-Za-z]+$/;

    
      }
    },

    validationMessage(){
        let message = "";
        if (!alphabet.test(this.username)) {
            message += "Please enter only alphabetic characters in the username field.";
        alert('Please enter only alphabetic characters in the username field.');
        
        this.username = '';
        }
    },

    async login() {
        if (this.username === "Admin" && this.password === 11) {
            console.log('logged in..!')
            this.$router.push('/HomeView');
        } else if (this.username === '' || this.password === '') {
            alert('Enter essential details');
        } else {
            console.log("Wrong..")
            alert("Wrong username or password..!");
        }
    }

    
    };
    





    

</script>


<style scoped>



.login-container {
  font-family: 'Gill Sans', sans-serif;
  background-image: url('~@/assets/crm.jpg');
  text-align: center;
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;   
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
  background-color: rgba(0, 0, 0, 0.5);
  margin: 20px auto;
  max-width: 400px;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
}

h1 {
  text-align: center;
  color: #333333;
}

label {
  font-family: "Georgia", Times, serif;
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

input {
  margin: 10px 0;
  width: 80%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

p{
 color: #333;   
}

button {
  background-color: #00d1d1;
  color: #ffffff;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  width: 50%;
}


</style>
