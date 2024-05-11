<template>
    <form @submit.prevent="login" class="login-form">
      <h3 id="sign">Sign in </h3>
      <!-- Email input -->
      <div class="form-control">
        <label for="Email">Email</label>
        <input type="email" id="Email" v-model="Email" placeholder="Enter your email address" required aria-label="Email address">
      </div>
      <!-- Password input -->
      <div class="form-control">
        <label for="password">Password</label>
        <input type="password" id="password" v-model="password" required placeholder="Enter your password" aria-label="Password">
        <p class="forgot-password"><a href="#" @click.prevent="forgotPassword">Forgot Password?</a></p>
      </div>
      <!-- Remember me checkbox -->
      <div class="form-control checkbox">
        <input type="checkbox" id="remember-me" v-model="rememberMe">
        <label for="remember-me">Keep me sign in for 30 days</label>
      </div>
      <!-- Sign in button -->
      <div class="btn">
        <button type="submit">Sign in</button>
      </div>
      <!-- External link -->
      <div class="extlink">
        <p>Read Our Terms and Services</p>
        <img src="@/assets/extlink.svg" alt="Global Distribution Logo ">
      </div>
    </form>
</template>

<script setup>
import { ref } from 'vue';

// Variables for form data
const Email = ref('');
const password = ref('');
const rememberMe = ref(false);

// Login function
const login = () => {
  // Basic client-side validation
  if (!Email.value || !password.value) {
    alert('Please enter both Email and password.');
    return;
  }
  
  // Simulating login process
  alert('Login Successful!');
};

// Forgot password function
const forgotPassword = () => {
  alert('Forgot Password clicked!');
};
</script>

<style scoped>



/* Form Styles */
#sign{
  margin-top: 0;
}
.login-form {
  
  border-radius: 5px;
  color: white;
  padding: 0 20px 0 20px ;
}

.login-form div {
  margin-bottom: 10px;

}

.login-form label {
  display: block;
  color: #1A68FF;
  margin-bottom: 5px;
  font-size: 14px;
  font-weight: 600;
}

.login-form input[type="email"],
.login-form input[type="password"] {
  width: 92%;
  padding: 10px;
  border: 2px solid #1C1C1E;
  background: #1c1c1e;
  color: white;
  box-shadow: 0 0 0 2px #2C2C2E;
  border-radius: 1px;
}

.login-form button {
  width: 100%;
  padding: 10px;
  border: none;
  border-radius: 3px;
  background-color: #007bff;
  color: #fff;
  cursor: pointer;
}

.forgot-password {
  text-align: end;
  font-weight: 400;
  font-size: 12px;
}

.forgot-password a {
  color: #BCBCBC;
  text-decoration: none;
}

.checkbox {
  display: flex;
  align-items: center;
}

.checkbox input[type="checkbox"] {
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 12px;
  height: 12px;
  margin-right: 2px;
  position: relative;
}

.checkbox input[type="checkbox"]::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid #BCBCBC;
  border-radius: 3px;
  background-color: transparent;
}

.checkbox input[type="checkbox"]:checked::after {
  content: "\2713";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}

.checkbox label {
  color: #BCBCBC;
  margin-left: 10px;
  margin-top: 7px;
  font-size: 12px;
}

/* External link Styles */
.extlink {
  display: flex;
  font-size: 12px;
  
}

.extlink img {
  margin: 10px;
  cursor: pointer;
}

/* Bottom Styles */


@media (max-width: 600px) {

  .extlink img {
  margin: 10px;

}
}

@media (max-width: 350px) {
  /* Add specific styles for smaller screens if needed */
}
</style>
