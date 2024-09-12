<template>
    <div>
        <h1>{{ name }}</h1>
        <h2>{{ title }}</h2>
        <h3>{{ description }}</h3>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const name = ref<string>('孙悟空')
const title = ref<string>('齐天大圣')
const description = ref<string>('在《西游记》中，孙悟空是一个勇敢无畏、机制聪明的角色，以其强大的能力和不屈的精神著称')
</script>

<style scoped>
div{
    box-shadow: 5px 5px 5px gray;
    border-radius: 1cap;
    padding: 5px;
    background-color: aquamarine;
}
h1 {
    color: red;
    width: 100%;
    text-align: center;
}
h2{
    color: blue;
    width: 100%;
    text-align: center;
}
h3{
    color: blueviolet;
    width: 100%;
    text-align: center;
}
</style>