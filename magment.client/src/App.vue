<template>    
    <div id="app">
        <div class="title">
            <div class="btn" @click="msg='Login'">登录</div>
            <div class="btn" @click="msg='Reg'">注册</div>
        </div>
        <component :is="msg"></component>
    </div>
</template>

<script lang="ts">
    //这里的from路径根据自己的布局更改路径
    import HelloWorld from './components/HelloWorld.vue'
    import TheWelcome from './components/TheWelcome.vue'
    import Login from '@/views/login.vue'
    import Reg from '@/views/register.vue'
    import {defineComponent} from 'vue';
    export default defineComponent({
        name: 'App',
            data() {
                return {
                    msg: "Login"
                }
            },
            components: {
                Login,
                Reg
            }
    });
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
    .title {
        text-align: center;
        background: #00ffff;
        width: 940px;
        height: 1180px;
        padding: 0 50px;
        position: absolute;
        top: 20px;
        right: 13px;
        bottom: 5px;
        left: 800px;
    }
    .btn {
        width: 260px;
        margin: 15px 20px;
        padding: 10px;
        border-radius: 15px;
        background-image: linear-gradient(to right, #a6c1ee, #fbc2eb);
        background-color: #fbc2eb;
        font: 16px;
        font-family: Arial;
        text-decoration: none;
        text-shadow: 0px 1px 0px #2f6627;
        column-rule:dashed;
    }
  
    .btn:hover {
        background-color: rgb(180,193,237);
    }

    .btn:active {
        position: relative;
        top: 5px;
    }
}
</style>
