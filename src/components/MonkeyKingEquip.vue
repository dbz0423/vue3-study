<template>
    <div>
        <h1>装备管理</h1>
        <div>
            <input type="text"  placeholder="输入装备名称" v-model="newEquipment.name">
            <button @click="addEquipment">添加装备</button>
        </div>
        <ul>
            <li v-for="(equipment , index) in equipmentList" :key="equipment.id">
                {{ equipment.name }}
                <button @click="deleteEquipment(index)">删除</button>
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
interface Equipment {
    id : number,
    name : string
}
const newEquipment = ref<Equipment>({
    id : 0  ,
    name : ""
})
const equipmentList = ref<Equipment[]>([])

const addEquipment = () => {
    if (newEquipment.value.name !== ""){
        equipmentList.value.push({ id : equipmentList.value.length , name : newEquipment.value.name})
        newEquipment.value = {id:0,name:""}
    }
}
const deleteEquipment = ( dId : number ) => {
    equipmentList.value = equipmentList.value.filter(equipment => equipment.id !== dId)
    for(let i = dId ; i< equipmentList.value.length ; i++){
        equipmentList.value[i].id = i;
    }
}



</script>

<style scoped>
div {
  text-align: center;
}

button {
    width: 100px;
    height: 50px;
    color: white;
    background-color: #2675FC;
    border: 0cap;
    margin: 10px;
    border-radius: 6px;
}

input {
    width: 300px;
    height: 50px;
    border-radius: 6px;
}

</style>