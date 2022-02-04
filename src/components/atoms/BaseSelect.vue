<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  id: string
  name: string
  options: string[]
  width: string
}

const props = defineProps<Props>()
const { label, id, options, width } = toRefs(props)
</script>

<template>
  <div class="select-wrapper">
    <label :for="id" class="label">{{ label }}</label>
    <div class="select">
      <select :id="id" :name="name">
        <option v-for="(option, index) in options" :key="index" :value="option">
          {{ option }}
        </option>
      </select>
    </div>
  </div>
</template>

<style scoped>
.select-wrapper {
  display: flex;
  flex-direction: column;
  width: v-bind(width);
}

.label {
  color: #818181;
}

.select {
  cursor: pointer;
  padding-left: 10px;
  border: 1px solid;
  border-radius: 5px;
  position: relative;
  z-index: 1;
}

.select::after {
  position: absolute;
  content: '';
  width: 8px;
  height: 8px;
  right: 10px;
  top: 50%;
  transform: translateY(-50%) rotate(45deg);
  border-bottom: 2px solid #818181;
  border-right: 2px solid #818181;
  z-index: -1;
}
</style>
