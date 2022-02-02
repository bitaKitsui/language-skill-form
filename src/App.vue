<script setup lang="ts">
import BaseInput from './components/atoms/BaseInput.vue'
import BaseTitle from './components/atoms/BaseTitle.vue'
import BaseSelect from './components/atoms/BaseSelect.vue'
import { LANGUAGE_LEVEL_SELECTS } from './constants'
import BaseButton from './components/atoms/BaseButton.vue'
import BaseIconButton from './components/atoms/BaseIconButton.vue'
</script>

<template>
  <BaseInput :id="'toeic'" :label="'Toeic'" :type="'text'" />
  <BaseInput :id="'toefl'" :label="'Toefl'" :type="'text'" />
  <BaseTitle :value="'語学力(英語)'" />
  <BaseSelect
    :id="'level'"
    :label="'レベル'"
    :name="'level-select'"
    :options="LANGUAGE_LEVEL_SELECTS"
  />
  <BaseButton :type="'button'" :label="'送信'" :color="'primary'" />
  <BaseIconButton
    :type="'button'"
    :label="'言語を追加する'"
    :color="'primary'"
    :outlined="true"
  />
</template>

<style></style>
