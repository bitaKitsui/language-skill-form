<script setup lang="ts">
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_SELECTS, LANGUAGE_LEVEL_SELECTS } from '../../constants'
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
}
</style>
