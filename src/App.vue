<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld /> -->
  <!-- <LoginPage /> -->
  <!-- <JsonToVue /> -->
  <!-- <PinySwitch /> -->
  <!-- <PinySwitch2 /> -->
  <!-- <CompThree /> -->
  <!-- <CompThree2 /> -->
  <Page1 />
  <Page2 />
  <!-- <Page3 /> -->
  <Page4 />
</template>

<script>
// import HelloWorld from './components/helloworld/HelloWorld.vue'
// import LoginPage from './components/LoginPage/index'
// import JsonToVue from './components/jsontoVue/index.vue'
// import PinySwitch from './components/pinySwitch/index.vue'
// import PinySwitch2 from './components/pinySwitch2/index.vue'
// import PinySwitch3 from './components/pinySwitch/index2.vue'
// import CompThree from './components/compThree/index.vue'
// import CompThree2 from './components/compThree/index2.vue'
import Page1 from './components/001-page'
import Page2 from './components/002-page'
// import Page3 from './components/003-mtd'
import Page4 from './components/004-page'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    // LoginPage,
    // JsonToVue,
    // PinySwitch,
    // PinySwitch2,
    // CompThree,
    // CompThree2,
    // PinySwitch3,
    Page1,
    Page2,
    // Page3,
    Page4,
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
