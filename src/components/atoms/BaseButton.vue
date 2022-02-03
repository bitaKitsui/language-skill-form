<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color: 'primary' | 'error' | 'disabled'
}

const props = defineProps<Props>()
const { label, type, color } = toRefs(props)
</script>

<template>
  <button :type="type" :color="color" class="button">
    {{ label }}
  </button>
</template>

<style scoped>
.button {
  cursor: pointer;
}
</style>
