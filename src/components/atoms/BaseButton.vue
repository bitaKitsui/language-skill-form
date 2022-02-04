<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color: 'primary' | 'error' | 'disabled'
  width: string
}

const props = defineProps<Props>()
const { label, type, color, width } = toRefs(props)
</script>

<template>
  <button :type="type" class="button">
    {{ label }}
  </button>
</template>

<style scoped>
.button {
  cursor: pointer;
  width: v-bind(width);
  text-align: center;
  border-radius: 4px;
}
</style>
