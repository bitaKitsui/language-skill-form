<script setup lang="ts">
import { reactive, toRefs } from 'vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseButtons from '../molecules/BaseButtons.vue'
import BaseFormList from '../molecules/BaseFormList.vue'

interface Props {
  width: string
}

const props = defineProps<Props>()
const { width } = toRefs(props)

const listItem = reactive([1])

const addListItem = () => listItem.push(listItem.length + 1)

const removeListItem = (key: number) => {
  if (listItem.length === 1) return
  // ボタンを押すと削除する機能
}
</script>

<template>
  <div class="other-language-wrapper">
    <BaseTitle :value="'語学力（その他言語）'" :width="'300px'" />
    <form class="other-language-form">
      <BaseFormList :list-item="listItem" @remove="removeListItem" />
      <BaseButtons @add="addListItem" />
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
