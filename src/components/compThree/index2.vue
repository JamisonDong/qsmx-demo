<template>
    <a-layout>
        <a-row :gutter="16">
            <a-col :span="12">
                <a-input v-model="inputValue" placeholder="请输入" />
            </a-col>
            <a-col :span="12">
                <a-select v-model="selectValue" placeholder="请选择">
                    <a-select-option v-for="(option, index) in selectOptions" :key="index" :value="option.value">{{
                        option.label }}</a-select-option>
                </a-select>
            </a-col>
        </a-row>
        <a-row :gutter="16">
            <a-col :span="12">
                <a-checkbox-group v-model="checkboxValue">
                    <a-checkbox v-for="(option, index) in checkboxOptions" :key="index" :value="option.value">{{
                        option.label }}</a-checkbox>
                </a-checkbox-group>
            </a-col>
            <a-col :span="12">
                <a-radio-group v-model="radioValue">
                    <a-radio v-for="(option, index) in radioOptions" :key="index" :value="option.value">{{ option.label
                    }}</a-radio>
                </a-radio-group>
            </a-col>
        </a-row>
        <a-row :gutter="16">
            <a-col :span="12">
                <a-date-picker v-model="dateValue" placeholder="请选择日期" />
            </a-col>
            <a-col :span="12">
                <a-button type="primary" @click="handleClick">查询</a-button>
            </a-col>
        </a-row>
        <a-table :columns="columns" :data-source="dataSource" />
    </a-layout>
</template>
  
<script>
import { defineComponent } from 'vue';
import { Layout, Row, Col, Button, Input, Select, Checkbox, Radio, DatePicker, Table } from 'ant-design-vue';

export default defineComponent({
    name: 'DemoPage',
    components: {
        'a-layout': Layout,
        'a-row': Row,
        'a-col': Col,
        'a-button': Button,
        'a-input': Input,
        'a-select': Select,
        'a-select-option': Select.Option,
        'a-checkbox-group': Checkbox.Group,
        'a-checkbox': Checkbox,
        'a-radio-group': Radio.Group,
        'a-radio': Radio,
        'a-date-picker': DatePicker,
        'a-table': Table,
    },
    data() {
        return {
            inputValue: '',
            selectValue: '',
            selectOptions: [
                { label: '选项一', value: 'option1' },
                { label: '选项二', value: 'option2' },
                { label: '选项三', value: 'option3' },
            ],
            checkboxValue: [],
            checkboxOptions: [
                { label: '选项一', value: 'option1' },
                { label: '选项二', value: 'option2' },
                { label: '选项三', value: 'option3' },
            ],
            radioValue: '',
            radioOptions: [
                { label: '选项一', value: 'option1' },
                { label: '选项二', value: 'option2' },
                { label: '选项三', value: 'option3' },
            ],
            dateValue: null,
            columns: [
                { title: '姓名', dataIndex: 'name', key: 'name' },
                { title: '年龄', dataIndex: 'age', key: 'age' },
                { title: '地址', dataIndex: 'address', key: 'address' },
            ],
            dataSource: [
                { key: '1', name: '张三', age: 18, address: '北京市海淀区' },
                { key: '2', name: '李四', age: 22, address: '上海市浦东新区' },
                { key: '3', name: '王五', age: 30, address: '广州市天河区' },
            ],
        };
    },
    methods: {
        handleClick() {
            console.log('查询按钮点击');
        },
    },
});
</script>