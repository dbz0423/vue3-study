<!-- <template>
    <div>
        <h1>当前形态：{{ status ? "斗战胜佛" : "齐天大圣" }}</h1>
        <button @click="changeStatus">切换形态</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const status = ref<boolean>(true)
const changeStatus = () => {
    status.value = !status.value
}
</script>

<style scoped>
div{
    text-align: center;
}
button{
    color: white;
    font-size: 20px;
    padding: 10px;
    background-color: coral;
    border-width: 0px;
    border-radius: 0.5cap;
}
</style> -->
<template>
    <div class="form-toggle">
        <h1>当前形态：{{ currentForm }}</h1>
        <button @click="toggleForm">切换形态</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const currentForm = ref('齐天大圣')
const toggleForm = () => {
    currentForm.value = currentForm.value === '齐天大圣' ? '斗战胜佛' : '齐天大圣'
}
</script>

<style scoped>
div{
    text-align: center;
}
button{
    color: white;
    font-size: 20px;
    padding: 10px;
    background-color: coral;
    border-width: 0px;
    border-radius: 0.5cap;
}
</style>