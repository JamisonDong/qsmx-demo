<template>
    <div class="pithy-switch">
        <a-switch :checked="checked" @change="handleChange" />
    </div>
</template>
  
<script>
import { defineComponent } from 'vue';
import { Switch } from 'ant-design-vue';

export default defineComponent({
    name: 'PithySwitch',
    components: {
        'a-switch': Switch,
    },
    data() {
        return {
            checked: false,
        };
    },
    methods: {
        handleChange(checked) {
            this.checked = checked;
        },
    },
});
</script>
  
<style scoped>
.pithy-switch {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}
</style>