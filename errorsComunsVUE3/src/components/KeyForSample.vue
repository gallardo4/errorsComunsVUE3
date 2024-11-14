<script setup>
import { shuffle } from 'lodash'
import { ref } from 'vue'

const items = ref([
  { id: 1, label: 'first name' },
  { id: 2, label: 'last name' },
  { id: 3, label: 'email' },
  { id: 4, label: 'website' }
])

function shuffleItems() {
  items.value = shuffle(items.value)
}
</script>

<template>
  <ul>
    <li v-for="item in items" :key="item.id">{{ item.label }} <!-- Afegim :key="item.id" per fixar un item -->
        <input type="text" />
    </li>
  </ul>
  <button @click="shuffleItems">Shuffle</button>
</template>