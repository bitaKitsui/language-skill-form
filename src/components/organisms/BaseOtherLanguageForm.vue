<script setup lang="ts">
import { toRefs } from 'vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseButtons from '../molecules/BaseButtons.vue'
import BaseSelects from '../molecules/BaseSelects.vue'

interface Props {
  width: string
}

const props = defineProps<Props>()
const { width } = toRefs(props)
</script>

<template>
  <div class="other-language-wrapper">
    <BaseTitle :value="'語学力（その他言語）'" :width="'300px'" />
    <form class="other-language-form">
      <div class="form-border">
        <div class="form-header">
          <BaseIconButton
            :label="'削除'"
            :type="'button'"
            color="'primary'"
            :outlined="false"
            :width="'60px'"
          />
        </div>
        <BaseSelects />
      </div>
      <BaseButtons />
    </form>
  </div>
</template>

<style scoped>
.other-language-wrapper {
  display: flex;
  height: auto;
}

.other-language-form {
  width: v-bind(width);
}

.form-border {
  border: 1px solid #3d60d5;
}

.form-header {
  width: 100%;
  height: 40px;
  background: #f2f3f7;
  display: flex;
  justify-content: flex-end;
}
</style>
