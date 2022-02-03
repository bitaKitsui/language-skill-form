<script setup lang="ts">
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseInput from '../atoms/BaseInput.vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_LEVEL_SELECTS } from '../../constants'
</script>

<template>
  <div class="form-wrapper">
    <BaseTitle :value="'語学力（英語）'" />
    <form class="form">
      <BaseSelect
        :id="'level'"
        :label="'レベル'"
        :name="'select-level'"
        :options="LANGUAGE_LEVEL_SELECTS"
      />
      <BaseInput :id="'toeic'" :label="'TOEIC'" :type="'text'" />
      <span>点</span>
      <BaseInput :id="'toefl'" :label="'TOEFL'" :type="'text'" />
      <span>点</span>
    </form>
  </div>
</template>

<style scoped>
.form-wrapper {
  display: flex;
  height: auto;
}

.form {
  display: flex;
}
</style>
