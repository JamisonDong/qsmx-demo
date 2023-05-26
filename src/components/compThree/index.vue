<template>
    <div>
        <a-switch :checked="switch1" @change="handleChange1" />
        <a-switch :checked="switch2" @change="handleChange2" />
    </div>
</template>
   
<script>
export default {
    name: 'newPage',
    data() {
        return {
            switch1: false,
            switch2: true,
        }
    },
    methods: {
        handleChange1(checked) {
            this.switch1 = checked
        },
        handleChange2(checked) {
            this.switch2 = checked
        },
    }
}
</script>