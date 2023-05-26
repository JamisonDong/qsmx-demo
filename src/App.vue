<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld />
  <LoginPage />
  <JsonToVue />
  <!-- <PinySwitch /> -->
  <PinySwitch2 />
  <CompThree />
  <CompThree2 />
</template>

<script>
import HelloWorld from './components/helloworld/HelloWorld.vue'
import LoginPage from './components/LoginPage/index'
import JsonToVue from './components/jsontoVue/index.vue'
// import PinySwitch from './components/pinySwitch/index.vue'
import PinySwitch2 from './components/pinySwitch2/index.vue'
import CompThree from './components/compThree/index.vue'
import CompThree2 from './components/compThree/index2.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    LoginPage,
    JsonToVue,
    // PinySwitch,
    PinySwitch2,
    CompThree,
    CompThree2,

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
