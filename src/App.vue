<script setup lang="ts">
import BaseInput from './components/atoms/BaseInput.vue'
import BaseTitle from './components/atoms/BaseTitle.vue'
</script>

<template>
  <BaseInput :id="'toeic'" :label="'Toeic'" :type="'text'" />
  <BaseInput :id="'toefl'" :label="'Toefl'" :type="'text'" />
  <BaseTitle :value="'語学力(英語)'" />
</template>

<style></style>
