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
  <div class="input">
    <label :for="id" class="label">{{ label }}</label>
    <div>
      <input :id="id" :type="type" :style="{ width }" />
      <span>点</span>
    </div>
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
