<template>
    <div class="container">
        <div class="login-wrapper">
            <div class="header">注册</div>
            <div class="form-wrapper">
                <input type="text" name="username" placeholder="账户" class="input-item">
                <input type="password" name="password" placeholder="密码" class="input-item">
                <input type="password" name="repassword" placeholder="再次确认密码" class="input-item">
                <div class="btn">注册</div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({

        components: {
            name: "Register"
        },
        directives: {
        },
        filters: {
        },
        props: {
        },
        data() {
            return {
            }
        },
        computed: {
        },
        watch: {
        },
        beforeCreate() {
        },
        created() {
        },
        beforeMount() {
        },
        mounted() {
        },
        updated() {
        },
        activated() {
        },
        deactivated() {
        },
        beforeDestroy() {
        },
        destroyed() {
        },
        methods: {
        },
    });
</script>

<style scoped>
    html {
        height: 100%;
    }

    body {
        height: 100%;
    }

    .container {
        /* margin-top: 5%; */
        width: 720px;
        height: 980px;
        position: absolute;
        top: 120px;
        right: 860px;
        bottom: 10px;
        left: 900px;
        background: #abc1ee;
        background-image: linear-gradient(to right, #fbc2eb, #a6c1ee);
        inline-size: stretch;
    }

    .login-wrapper {
        background-color: #b6ff00;
        width: 560px;
        height: 888px;
        border-radius: 15px;
        padding: 0 50px;
        position: absolute;
        top: 480px;
        right: 600px;
        bottom: 10px;
        left: 340px;
        transform: translate(-50%, -50%);
        inline-size: stretch;
    }
    .header {
        font-size: 38px;
        font-weight: bold;
        text-align: center;
        line-height: 200px;
    }

    .input-item {
        display: block;
        width: 100%;
        margin-bottom: 20px;
        border: 0;
        padding: 10px;
        border-bottom: 1px solid rgb(128, 125, 125);
        font-size: 15px;
        outline: none;
    }

        .input-item:placeholder-shown {
            text-transform: uppercase;
        }

    .btn {
        text-align: center;
        padding: 10px;
        width: 100%;
        margin-top: 40px;
        background-image: linear-gradient(to right, #a6c1ee, #fbc2eb);
        border-radius: 15px;
        color: #fff;
        margin: 0 auto;
    }
    .btn:hover {
        background-color: rgb(180,193,237);
    }

    .btn:active {
        position: relative;
        top: 1px;
    }
    .msg {
        text-align: center;
        line-height: 88px;
    }

    a {
        text-decoration-line: none;
        color: #abc1ee;
    }
</style>