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
    <slot name="named" :namedText="props.greetingMessage"></slot>
  </div>
</template>
