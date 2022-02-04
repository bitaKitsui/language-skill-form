<script setup lang="ts">
import { toRefs } from 'vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseInput from '../atoms/BaseInput.vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_LEVEL_SELECTS } from '../../constants'

interface Props {
  width: string
}

const props = defineProps<Props>()
const { width } = toRefs(props)
</script>

<template>
  <div class="form-wrapper">
    <BaseTitle :value="'語学力（英語）'" :width="'300px'" />
    <form class="form">
      <BaseSelect
        :id="'level'"
        :label="'レベル'"
        :name="'select-level'"
        :options="LANGUAGE_LEVEL_SELECTS"
        :width="'200px'"
      />
      <BaseInput
        :id="'toeic'"
        :label="'TOEIC'"
        :type="'text'"
        :width="'80px'"
      />
      <BaseInput
        :id="'toefl'"
        :label="'TOEFL'"
        :type="'text'"
        :width="'80px'"
      />
    </form>
  </div>
</template>

<style scoped>
.form-wrapper {
  display: flex;
  height: auto;
  padding-bottom: 30px;
}

.form {
  display: flex;
  justify-content: space-between;
  border: 1px solid;
  width: v-bind(width);
}
</style>
