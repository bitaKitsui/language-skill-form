<script setup lang="ts">
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div class="buttons">
    <BaseIconButton
      :label="'言語を追加'"
      :type="'button'"
      :color="'primary'"
      :outlined="true"
      :width="'150px'"
    />
    <BaseButton
      :label="'送信'"
      :type="'submit'"
      :color="'primary'"
      :width="'100px'"
    />
  </div>
</template>

<style scoped>
.buttons {
  display: flex;
}
</style>
