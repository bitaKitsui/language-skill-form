<script setup lang="ts">
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseButton from '../atoms/BaseButton.vue'

interface Emits {
  (event: 'add'): void
}

const emits = defineEmits<Emits>()

const handleClick = () => {
  emits('add')
}
</script>

<template>
  <div class="buttons">
    <div class="buttons__icon-button">
      <BaseIconButton
        :label="'言語を追加'"
        :icon="'+'"
        :type="'button'"
        :color="'primary'"
        :outlined="true"
        :width="'150px'"
        @add="handleClick"
      />
    </div>
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
  height: 40px;
}

.buttons__icon-button {
  margin-right: 40px;
}
</style>
