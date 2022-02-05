<script setup lang="ts">
import { toRefs } from 'vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_SELECTS, LANGUAGE_LEVEL_SELECTS } from '../../constants'

interface Props {
  height: string
}

const props = defineProps<Props>()
const { height } = toRefs(props)
</script>

<template>
  <div class="form-selects">
    <BaseSelect
      :id="'language'"
      :label="'言語'"
      :name="'select-language'"
      :options="LANGUAGE_SELECTS"
      :width="'200px'"
    />
    <BaseSelect
      :id="'level'"
      :label="'レベル'"
      :name="'select-level'"
      :options="LANGUAGE_LEVEL_SELECTS"
      :width="'200px'"
    />
  </div>
</template>

<style scoped>
.form-selects {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: v-bind(height);
}
</style>
