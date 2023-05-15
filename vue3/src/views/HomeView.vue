<script setup></script>

<template>
  <div class="home">
    <button class="btn" @click="decreaseCounter">-</button>
    <span class="counter"> {{ counter }}</span>

    <button class="btn" @click="increaseCounter">+</button>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const counter = ref(10)

    const increaseCounter = () => {
      counter.value++
    }

    const decreaseCounter = () => {
      counter.value--
    }
    return {
      counter,
      increaseCounter,
      decreaseCounter
    }
  }
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
</style>
