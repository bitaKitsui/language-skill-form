<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color: 'primary' | 'error' | 'disabled'
  outlined: boolean
}

const props = defineProps<Props>()
const { label, type, color, outlined } = toRefs(props)
</script>

<template>
  <button :type="type" :color="color" :outlined="outlined" class="icon-button">
    <span>+</span>
    <span>
      {{ label }}
    </span>
  </button>
</template>

<style scoped>
.icon-button {
  cursor: pointer;
}
</style>
