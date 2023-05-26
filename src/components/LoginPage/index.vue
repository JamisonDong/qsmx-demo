<template>
    <div class="container">
        <h1>Login</h1>
        <a-form @submit="handleSubmit">
            <a-form-item label="Username" required>
                <a-input v-model="username" />
            </a-form-item>
            <a-form-item label="Password" required>
                <a-input v-model="password" type="password" />
            </a-form-item>
            <a-form-item>
                <a-button type="primary" html-type="submit">Login</a-button>
                <a-button @click="handleRegister" id="register-btn">Register</a-button>
            </a-form-item>
        </a-form>
    </div>
</template>
  
<script>
import { defineComponent } from 'vue';
import { Form, Input, Button } from 'ant-design-vue';

export default defineComponent({
    name: 'LoginPage',
    components: {
        'a-form': Form,
        'a-form-item': Form.Item,
        'a-input': Input,
        'a-button': Button,
    },
    data() {
        return {
            username: '',
            password: '',
        };
    },
    methods: {
        handleSubmit(e) {
            e.preventDefault();
            // 处理登录逻辑
        },
        handleRegister() {
            // 处理注册逻辑
            this.$message.success('Register button clicked!');
        },
    },
});
</script>
  
<style>
.container {
    margin: 100px auto;
    width: 400px;
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
}

h1 {
    text-align: center;
    margin-bottom: 30px;
}

.a-form-item {
    margin-bottom: 20px;
}

#register-btn {
    background-color: #ccc;
    color: #fff;
}

#register-btn:hover {
    background-color: #b3b3b3;
}
</style>