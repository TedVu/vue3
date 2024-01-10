<script setup>
defineProps({
  firstName: String,
  lastName: String
})

defineEmits(['update:firstName', 'update:lastName'])
</script>

<template>
  <div>Child Component First Name:</div>
  <input type="text" :value="firstName" @input="$emit('update:firstName', $event.target.value)" />
  <div>Child Component Last Name:</div>
  <input type="text" :value="lastName" @input="$emit('update:lastName', $event.target.value)" />
</template>
