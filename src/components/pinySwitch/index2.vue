<template>
    <div>
        <a-card>
            <a-row :gutter="16">
                <a-col :span="12">
                    <div class="switch-bg"
                        :style="{ left: bgFrame.x, top: bgFrame.y, width: bgFrame.width, height: bgFrame.height }"></div>
                </a-col>
                <a-col :span="12">
                    <a-switch :checked="checked" :loading="loading" :disabled="disabled" @change="handleChange"
                        :style="{ left: btnFrame.x, top: btnFrame.y }"></a-switch>
                </a-col>
            </a-row>
        </a-card>
    </div>
</template>
  
<script>
import { Switch, Row, Col, Card } from 'ant-design-vue';

export default {
    name: 'PithySwitch',
    components: {
        'a-switch': Switch,
        'a-row': Row,
        'a-col': Col,
        'a-card': Card,
    },
    data() {
        return {
            checked: true,
            loading: false,
            disabled: false,
            bgFrame: {
                x: 0,
                y: 0,
                width: 100,
                height: 50,
            },
            btnFrame: {
                x: 50,
                y: 10,
                width: 40,
                height: 30,
            },
        };
    },
    methods: {
        handleChange(checked) {
            console.log(`switch to ${checked}`);
        },
    },
};
</script>
  
<style scoped>
.switch-bg {
    position: absolute;
    background-color: #ccc;
    border-radius: 25px;
}
</style>