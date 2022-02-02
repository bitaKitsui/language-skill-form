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
  <div>
    <button :type="type" :color="color" :outlined="outlined">
      <span>+</span>
      <span>
        {{ label }}
      </span>
    </button>
  </div>
</template>
