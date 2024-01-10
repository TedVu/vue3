<template>
  <div>
    <ChildComponent v-model:first-name="counterData.title" v-model:last-name="counterData.title" />
    <div>
      <input v-model="counterData.title" />
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
import ChildComponent from '../components/ChildComponent.vue'

const counterData = reactive({
  title: 'My Counter'
})
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
