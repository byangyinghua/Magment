<template>
    <div class="ValidCode disabled-select"
         :style="width:80px; height:40px"
         @click="refreshCode">
        <span v-for="(item, index) in codeList"
              :key="index"
              :style="getStyle(item)">
            {{item.code}}
        </span>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({     
        name: "Login",
        components: {
            ValidCode;
        },
        model: {
            prop: 'value',
            event: 'input'
        },
        directives: {
        },
        filters: {
        },
        props: {
            width: {
                  type: String,
                  default: '100px'
            },
            height: {
                  type: String,
                  default: '34px'
            },
            length: {
                  type: Number,
                  default: 4
            }   
        },
        data() {
            return {
                codeList: []
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
            this.createdCode()
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
            refreshCode () {
              this.createdCode()
            },
            createdCode () {
                  const len = this.length
                  const codeList = []
                  const chars = 'ABCDEFGHJKMNPQRSTWXYZabcdefhijkmnprstwxyz0123456789'
                  const charsLen = chars.length
                  // 生成
                  for (let i = 0; i < len; i++) {
                        const rgb = [Math.round(Math.random() * 220), Math.round(Math.random() * 240), Math.round(Math.random() * 200)]
                        codeList.push({
                          code: chars.charAt(Math.floor(Math.random() * charsLen)),
                          color: `rgb(${rgb})`,
                          fontSize: `1${[Math.floor(Math.random() * 10)]}px`,
                          padding: `${[Math.floor(Math.random() * 10)]}px`,
                          transform: `rotate(${Math.floor(Math.random() * 90) - Math.floor(Math.random() * 90)}deg)`
                        })
                    }
              // 指向
              this.codeList = codeList
              // 将当前数据派发出去
              this.$emit('input', codeList.map(item => item.code).join(''))
            },
            getStyle (data) {
                return `color: ${data.color}; font-size: ${data.fontSize}; padding: ${data.padding}; transform: ${data.transform}`
            }
        }
    });
</script>

<style scoped>
    ValidCode {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
    }
    span{
        display: inline-block;
    }   
   
</style>