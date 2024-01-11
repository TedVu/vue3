<script setup>
const props = defineProps({
  modelValue: String,
  greetingMessage: {
    type: String,
    default: 'Hello World!'
  },
  modelModifiers: { default: () => ({}) }
})
</script>

<!-- <MyComponent> template -->
<template>
  <div>
    <slot :text="props.greetingMessage" :count="1">Fallback</slot>
  </div>
</template>
