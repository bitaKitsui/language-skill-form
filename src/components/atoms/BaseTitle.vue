<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  value: string
  width: string
}

const props = defineProps<Props>()
const { value, width } = toRefs(props)
</script>

<template>
  <p class="title">
    {{ value }}
  </p>
</template>

<style scoped>
.title {
  color: #818181;
  width: v-bind(width);
}
</style>
