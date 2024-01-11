<template>
  <div>
    <div>Value from parent is {{ counterData.title }}</div>
    <ChildComponent v-model.capitalize="counterData.title"
      >Some slot content displayed
      <template v-slot:namedSlot> Header named slot </template>
      <template #[slotName]></template>
    </ChildComponent>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'
import ChildComponent from '../components/ChildComponent.vue'

const counterData = reactive({
  title: 'My Counter'
})

const slotName = ref('dynamicSlotName')
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
