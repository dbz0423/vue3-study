<template>
    <div class="total">
        <div class="item1">
            基础攻击力：
            <input v-model="baseAttack" type="number" />
        </div>
        <div class="item2">
            装备加成：
            <input v-model="gearBonus" type="number" />            
        </div>
        <p>总攻击力：{{ totalAttack }}</p>
    </div>

    
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';

const baseAttack = ref<number>(50)
const gearBonus = ref<number>(20)

const totalAttack = computed(() => {
    return baseAttack.value + gearBonus.value
})
</script>

<style scoped>

.total {
    width: 100%;
    text-align: center;
    background-color: lightblue;
}

.item1 {
    margin: 10px;
}

.item2 {
    margin: 10px;
}
</style>