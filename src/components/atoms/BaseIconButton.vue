<script setup lang="ts">
import { computed, toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color: 'primary' | 'error' | 'disabled'
  outlined: boolean
  width: string
}

const props = defineProps<Props>()
const { label, type, color, outlined, width } = toRefs(props)

const classObject = computed(() => {
  return {
    'icon-button--outlined': outlined.value,
    'icon-button': !outlined.value,
  }
})
</script>

<template>
  <button :type="type" :class="classObject">
    <span>+</span>
    <span>
      {{ label }}
    </span>
  </button>
</template>

<style scoped>
.icon-button {
  cursor: pointer;
  border: none;
  width: v-bind(width);
  text-align: center;
}

.icon-button:hover {
  border: 1px solid #056394;
}

.icon-button--outlined {
  border: 1px solid #056394;
  border-radius: 4px;
  color: #056394;
  cursor: pointer;
  width: v-bind(width);
  text-align: center;
}
</style>
