<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld />
  <LoginPage />
</template>

<script>
import HelloWorld from './components/helloworld/HelloWorld.vue'
import LoginPage from './components/LoginPage/index'

export default {
  name: 'App',
  components: {
    HelloWorld,
    LoginPage,
  }
}
</script>

<style>
@import '~ant-design-vue/dist/antd.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
