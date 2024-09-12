<template>
    <div>
        <h1>技能列表</h1>
        <li v-for="(skill , index) in skills" :key="skill.id" > 
            {{ skill.name }}  --- 
            <span v-if="skill.status" style="color: green;">已解锁</span> 
            <span v-else style="color: red;">未解锁</span>
        </li>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface Skill {
    id : number
    name : string,
    status : boolean 
} 

const skills = ref<Skill[]>([
    { id : 1 , name: '七十二变' , status : true},
    { id : 2 , name: '火眼金睛' , status : false},
    { id : 3 , name: '筋斗云' , status : true},
])
</script>

<style scoped>
li{
    margin: 10px;
}
</style>