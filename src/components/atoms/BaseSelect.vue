<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  id: string
  name: string
  options: string[]
}

const props = defineProps<Props>()
const { label, id, options } = toRefs(props)
</script>

<template>
  <div class="select">
    <label :for="id" class="label">{{ label }}</label>
    <select :id="id" :name="name">
      <option v-for="(option, index) in options" :key="index" :value="option">
        {{ option }}
      </option>
    </select>
  </div>
</template>

<style scoped>
.select {
  display: flex;
  flex-direction: column;
}

.label {
  color: #818181;
}
</style>
