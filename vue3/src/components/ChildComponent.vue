<template>
  <div>{{ value }}</div>
</template>

<script setup lang="ts">
import { watch } from 'vue'

const props = defineProps({
  value: {
    type: String,
    default: ''
  }
})

watch(
  () => props.value,
  (newValue) => {
    console.log(`New value is ${newValue}`)
  }
)
</script>
