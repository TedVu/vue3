<template>
  <div>
    <ChildComponent />
    <input type="text" v-model="title" />
  </div>
</template>

<script setup>
import { provide, ref } from 'vue'
import ChildComponent from '../components/ChildComponent.vue'

const title = ref('ted')

provide('title', title)
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
