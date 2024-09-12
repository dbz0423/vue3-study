<template>
    <div>
        <p>血量：{{ last }}/{{ total }}({{ hpPercentage }}%)</p>
        <meter :value="last" min="0" :max="total"></meter>
    </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';
const total = ref<number>(100)
const last = ref<number>(70)

const hpPercentage  = computed<number>(() => {
    return last.value / total.value * 100
})
</script>

<style scoped>
div {
  text-align: center;
}

meter {
  width: 500px;
  height: 30px;
}

</style>