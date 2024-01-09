<template>
  <div>{{ modelValue }}</div>
</template>

<script setup lang="ts">
import { watch } from 'vue'

const props = defineProps({
  modelValue: {
    type: String,
    default: ''
  }
})

watch(
  () => props.modelValue,
  (newValue) => {
    console.log(`New value is ${newValue}`)
  }
)
</script>
