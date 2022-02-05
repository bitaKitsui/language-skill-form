<script setup lang="ts">
import { toRefs } from 'vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseButtons from '../molecules/BaseButtons.vue'
import BaseFormList from '../molecules/BaseFormList.vue'

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
      <BaseFormList />
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
</style>
