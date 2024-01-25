<script setup>
import { inject } from 'vue'
const title = inject('title')
</script>

<template>
  <div>Hello {{ title }}</div>
</template>
