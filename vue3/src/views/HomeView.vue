<script setup></script>

<template>
  <h3>{{ counterTitle }}</h3>
  <div class="home">
    <button class="btn" @click="decreaseCounter">-</button>
    <span class="counter"> {{ counter }}</span>

    <button class="btn" @click="increaseCounter">+</button>
  </div>
  <div class="edit">
    <h4>Edit counter title:</h4>
    <input v-model="counterTitle" type="text" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
const counter = ref(10),
  counterTitle = ref('Counter Title')

const increaseCounter = () => {
  counter.value++
}

const decreaseCounter = () => {
  counter.value--
}
</script>

<style>
.home {
  text-align: center;
}

.btn,
.counter {
  font-size: 40px;
  margin: 10px;
}
.edit {
  margin-top: 60px;
}
</style>
