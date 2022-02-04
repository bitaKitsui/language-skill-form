<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  id: string
  type: HTMLInputElement
  width: string
}

const props = defineProps<Props>()
const { label, id, type, width } = toRefs(props)
</script>

<template>
  <div class="input-wrapper">
    <label :for="id" class="label">{{ label }}</label>
    <div>
      <input :id="id" :type="type" class="input" />
      <span>点</span>
    </div>
  </div>
</template>

<style scoped>
.input-wrapper {
  display: flex;
  flex-direction: column;
}

.label {
  color: #818181;
}

.input {
  width: v-bind(width);
}
</style>
