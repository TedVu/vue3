<script setup></script>

<template>
  <h3>{{ counterData.title }}</h3>
  <div class="home">
    <button class="btn" @click="decreaseCounter">-</button>
    <span class="counter"> {{ counterData.count }}</span>

    <button class="btn" @click="increaseCounter">+</button>
  </div>
  <div class="edit">
    <h4>Edit counter title:</h4>
    <input v-model="counterData.title" type="text" />
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const counterData = reactive({
  count: 0,
  title: 'My Counter'
})

const increaseCounter = () => {
  counterData.count++
}

const decreaseCounter = () => {
  counterData.count--
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
