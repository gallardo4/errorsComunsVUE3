<script setup>
import { ref, watch } from 'vue'

const numbers = ref([])
watch(numbers, (numbers) => console.log(numbers), { deep: true })

const randomNum = () => numbers.value.push(Math.random())
</script>

<template>
  <button @click="randomNum">Add Random Number</button>
</template>
