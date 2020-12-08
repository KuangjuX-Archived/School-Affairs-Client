<!-- home -->
<template>
  <div class="login-container">
    <div class="login-title">天津大学校务专区</div>
    <van-form @submit="onSubmit" class="login-form">
      <van-field
        v-model="username"
        name="用户名"
        input-align="center"
        error-message-align="center"
        placeholder="用户名"
        :rules="[{ required: true }]"
      />
      <van-field
        v-model="password"
        type="password"
        name="密码"
        input-align="center"
        error-message-align="center"
        placeholder="密码"
        :rules="[{ required: true }]"
      />
      <van-button class="login-button" block color="#00a0e9" native-type="submit"> 登录 </van-button>
      <div class="login-funcbar">
        <router-link to="/forget" class="func-item">忘记密码</router-link>
        <router-link to="/signup" class="func-item">没有账号？注册一个</router-link>
      </div>
    </van-form>
    <img class="login-footer" src="@/assets/logo.svg" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    onSubmit(values) {
      console.log('submit', values)
    }
  }
}
</script>
<style lang="scss" scoped>
.login-container {
  display: flex;
  height: 100vh;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .login-form {
    width: 80%;
    .login-button {
      margin-top: 20px;
    }
    .login-funcbar {
      display: flex;
      justify-content: space-between;
      margin-top: 10px;
      .func-item {
        color: #00a0e9;
        font-size: 14px;
        cursor: pointer;
      }
      .func-item:hover {
        opacity: 0.6;
      }
    }
  }

  .login-title {
    font-size: 24px;
    margin-bottom: 25px;
  }
  .login-footer {
    display: block;
    height: 30px;
    position: absolute;
    bottom: 20px;
  }
}
</style>
