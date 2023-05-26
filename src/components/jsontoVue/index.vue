<template>
    <div class="ant-switch" :class="{ 'ant-switch-checked': checked }" @click="toggle">
      <div class="ant-switch-inner">
        <div class="ant-switch-background">
          <div class="ant-switch-handle"></div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AntSwitch',
    data() {
      return {
        checked: false
      }
    },
    methods: {
      toggle() {
        this.checked = !this.checked
      }
    }
  }
  </script>
  
  <style scoped>
  .ant-switch {
    position: relative;
    display: inline-block;
    width: 40px;
    height: 20px;
    line-height: 20px;
    vertical-align: middle;
    background-color: #f1f1f1;
    border-radius: 20px;
    cursor: pointer;
    transition: all 0.3s;
  }
  
  .ant-switch-checked {
    background-color: #1890ff;
  }
  
  .ant-switch-inner {
    position: relative;
    display: inline-block;
    width: 100%;
    height: 100%;
  }
  
  .ant-switch-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 20px;
    background-color: #fff;
    transition: all 0.3s;
  }
  
  .ant-switch-checked .ant-switch-background {
    background-color: #fff;
    transform: translateX(-20px);
  }
  
  .ant-switch-handle {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 18px;
    height: 18px;
    border-radius: 50%;
    background-color: #fff;
    box-shadow: 0 2px 2px rgba(0, 0, 0, 0.2);
    transition: all 0.3s;
  }
  
  .ant-switch-checked .ant-switch-handle {
    transform: translateX(20px);
  }
  </style>