<script setup lang="ts">
import { computed, toRefs } from 'vue'

interface Props {
  label: string
  icon: string
  type: HTMLButtonElement
  color: 'primary' | 'error' | 'disabled'
  outlined: boolean
  width: string
}

interface Emits {
  (event: 'add'): void
  (event: 'remove'): void
}

const props = defineProps<Props>()
const { label, icon, type, color, outlined, width } = toRefs(props)

const classObject = computed(() => {
  return {
    outlined: outlined.value,
    text: !outlined.value,
  }
})

const emits = defineEmits<Emits>()

const onClick = () => {
  if (label.value === '削除') emits('remove')
  if (label.value === '言語を追加') emits('add')
}
</script>

<template>
  <button :type="type" :class="['icon-button', classObject]" @click="onClick">
    <span>{{ icon }}</span>
    <span>
      {{ label }}
    </span>
  </button>
</template>

<style scoped>
.icon-button {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100%;
}

.text {
  cursor: pointer;
  border: none;
  width: v-bind(width);
  color: #3d60d5;
}

.text:hover {
  border: 1px solid #3d60d5;
}

.outlined {
  border: 1px solid #3d60d5;
  border-radius: 4px;
  color: #3d60d5;
  cursor: pointer;
  width: v-bind(width);
  text-align: center;
}
</style>
