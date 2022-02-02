<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  id: string
  type: HTMLInputElement
}

const props = defineProps<Props>()
const { label, id, type } = toRefs(props)
</script>

<template>
  <div class="input">
    <label :for="id" class="label">{{ label }}</label>
    <input :id="id" :type="type" />
  </div>
</template>

<style scoped>
.input {
  display: flex;
  flex-direction: column;
}

.label {
  color: #818181;
}
</style>
