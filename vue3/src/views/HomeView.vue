<template>
  <div>
    <ChildComponent>
      <template #named="{ namedText }">This is a named slot {{ namedText }}</template>
    </ChildComponent>
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
