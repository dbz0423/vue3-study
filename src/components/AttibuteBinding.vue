<template>
    <div>
        <!-- 绑定 isDisabled 属性 -->
        <!-- <button v-bind="isDisabled">点击</button> -->
        <button :disabled="isDisabled">点击</button>
        <img src="@/assets/images/example.jpg">
        <button v-bind="buttonAttrs">点击我</button>
    </div>
</template>

<script setup lang="ts">
import { reactive, ref } from 'vue'
const isDisabled = ref<boolean>(false)

const buttonAttrs = reactive({
    disabled:false,
    title:"按钮已禁用",
    id:'unique-button'
})
</script>

<style scoped>

</style>