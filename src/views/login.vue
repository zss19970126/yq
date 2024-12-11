<template>
  <div class="login-container">
    <h2>登录</h2>
    <form @submit.prevent="handleLogin">
      <div class="form-group">
        <label for="username">用户名</label>
        <input type="text" id="username" v-model="username" required />
      </div>
      <div class="form-group">
        <label for="password">密码</label>
        <input type="password" id="password" v-model="password" required />
      </div>
      <button type="submit" class="login-button">登录</button>
    </form>
  </div>
  <div class="snowflakes">
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
    <div class="snowflake">
      <img src="https://i.pinimg.com/originals/65/05/77/650577673fad701100d239c52fb6f044.gif" width="50">
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const username = ref('');
const password = ref('');
const router = useRouter();

const handleLogin = () => {
  // 这里可以添加登录逻辑，例如调用 API 验证用户名和密码
  console.log('Username:', username.value);
  console.log('Password:', password.value);

  // 假设登录成功，跳转到首页
  router.push('/home');
};
</script>

<style scoped>
.login-container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

.login-button {
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.login-button:hover {
  background-color: #0056b3;
}


/*背景 */

body {
  background: #ededed;
}

/* customizable snowflake styling */
.snowflake {
  color: #fff;
  font-size: 1em;
  font-family: Arial;
  text-shadow: 0 0 1px #000;
}

@-webkit-keyframes snowflakes-fall {
  0% {
    top: -10%
  }

  100% {
    top: 100%
  }
}

@-webkit-keyframes snowflakes-shake {
  0% {
    -webkit-transform: translateX(0px);
    transform: translateX(0px)
  }

  50% {
    -webkit-transform: translateX(80px);
    transform: translateX(80px)
  }

  100% {
    -webkit-transform: translateX(0px);
    transform: translateX(0px)
  }
}

@keyframes snowflakes-fall {
  0% {
    top: -10%
  }

  100% {
    top: 100%
  }
}

@keyframes snowflakes-shake {
  0% {
    transform: translateX(0px)
  }

  50% {
    transform: translateX(80px)
  }

  100% {
    transform: translateX(0px)
  }
}

.snowflake {
  position: fixed;
  top: -10%;
  z-index: 9999;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  cursor: default;
  -webkit-animation-name: snowflakes-fall, snowflakes-shake;
  -webkit-animation-duration: 10s, 3s;
  -webkit-animation-timing-function: linear, ease-in-out;
  -webkit-animation-iteration-count: infinite, infinite;
  -webkit-animation-play-state: running, running;
  animation-name: snowflakes-fall, snowflakes-shake;
  animation-duration: 10s, 3s;
  animation-timing-function: linear, ease-in-out;
  animation-iteration-count: infinite, infinite;
  animation-play-state: running, running
}

.snowflake:nth-of-type(0) {
  left: 1%;
  -webkit-animation-delay: 0s, 0s;
  animation-delay: 0s, 0s
}

.snowflake:nth-of-type(1) {
  left: 10%;
  -webkit-animation-delay: 1s, 1s;
  animation-delay: 1s, 1s
}

.snowflake:nth-of-type(2) {
  left: 20%;
  -webkit-animation-delay: 6s, .5s;
  animation-delay: 6s, .5s
}

.snowflake:nth-of-type(3) {
  left: 30%;
  -webkit-animation-delay: 4s, 2s;
  animation-delay: 4s, 2s
}

.snowflake:nth-of-type(4) {
  left: 40%;
  -webkit-animation-delay: 2s, 2s;
  animation-delay: 2s, 2s
}

.snowflake:nth-of-type(5) {
  left: 50%;
  -webkit-animation-delay: 8s, 3s;
  animation-delay: 8s, 3s
}

.snowflake:nth-of-type(6) {
  left: 60%;
  -webkit-animation-delay: 6s, 2s;
  animation-delay: 6s, 2s
}

.snowflake:nth-of-type(7) {
  left: 70%;
  -webkit-animation-delay: 2.5s, 1s;
  animation-delay: 2.5s, 1s
}

.snowflake:nth-of-type(8) {
  left: 80%;
  -webkit-animation-delay: 1s, 0s;
  animation-delay: 1s, 0s
}

.snowflake:nth-of-type(9) {
  left: 90%;
  -webkit-animation-delay: 3s, 1.5s;
  animation-delay: 3s, 1.5s
}

/* Demo Purpose Only*/
.demo {
  font-family: 'Raleway', sans-serif;
  color: #fff;
  display: block;
  margin: 0 auto;
  padding: 15px 0;
  text-align: center;
}

.demo a {
  font-family: 'Raleway', sans-serif;
  color: #000;
}
</style>