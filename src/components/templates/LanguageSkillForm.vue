<script setup lang="ts">
import BaseForm from '../molecules/BaseForm.vue'
import BaseOtherLanguageForm from '../molecules/BaseOtherLanguageForm.vue'
</script>

<template>
  <div class="wrapper">
    <BaseForm :width="'650px'" />
    <BaseOtherLanguageForm :width="'800px'" />
  </div>
</template>

<style scoped>
.wrapper {
  margin-top: 30px;
  margin-left: 100px;
}
</style>
