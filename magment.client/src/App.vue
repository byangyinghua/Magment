<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
    <header>
        <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

        <div class="wrapper">
            <HelloWorld msg="You did it!" />
        </div>
    </header>
    <div id="app">
        <div class="title">
            <div class="btn" @click="msg='Login'">登录</div>
            <div class="btn" @click="msg='Reg'">注册</div>
        </div>
        <component :is="msg"></component>
    </div>
</template>

<script>
    //这里的from路径根据自己的布局更改路径
    import Login from '@/views/login.vue'
    import Reg from '@/views/register.vue'
    export default {
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
    }
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

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
