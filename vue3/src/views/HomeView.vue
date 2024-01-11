<template>
  <div>
    <ChildComponent v-slot="{ text, count }"> {{ text }} {{ count }} </ChildComponent>
  </div>
</template>

<script setup>
import ChildComponent from '../components/ChildComponent.vue'
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
