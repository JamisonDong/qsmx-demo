<template>
    <div id="app">
        <h1>MTD Sketch</h1>
        <mtd-button @click="increaseCount">Click me to increase count!</mtd-button>
        <p>Current count is {{ count }}</p>
        <mtd-input :value="inputValue" @change="updateInputValue"></mtd-input>
        <mtd-checkbox :checked="isChecked" @change="toggleCheck">Check me</mtd-checkbox>
    </div>
</template>
  
<script>
import { Button, Checkbox, Input } from '@ss/mtd-vue';

export default {
    name: 'App',
    components: {
        MtdButton: Button,
        MtdCheckbox: Checkbox,
        MtdInput: Input
    },
    data() {
        return {
            count: 0,
            inputValue: '',
            isChecked: false
        };
    },
    methods: {
        increaseCount() {
            this.count += 1;
        },
        updateInputValue(event) {
            this.inputValue = event.target.value;
        },
        toggleCheck(event) {
            this.isChecked = event.target.checked;
        }
    }
};
</script>