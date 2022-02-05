<script setup lang="ts">
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseSelects from '../molecules/BaseSelects.vue'
</script>

<template>
  <ul class="form-list">
    <li class="form-border">
      <div class="form-header">
        <BaseIconButton
          :label="'削除'"
          :icon="'×'"
          :type="'button'"
          color="'primary'"
          :outlined="false"
          :width="'80px'"
        />
      </div>
      <BaseSelects :height="'170px'" />
    </li>
  </ul>
</template>

<style scoped>
.form-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

.form-border {
  border: 1px solid #3d60d5;
  margin-bottom: 20px;
}

.form-header {
  width: 100%;
  height: 40px;
  background: #f2f3f7;
  display: flex;
  justify-content: flex-end;
}
</style>
