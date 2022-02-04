<script setup lang="ts">
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_SELECTS, LANGUAGE_LEVEL_SELECTS } from '../../constants'
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div class="other-language-wrapper">
    <BaseTitle :value="'語学力（その他言語）'" :width="'300px'" />
    <form class="other-language-form">
      <BaseIconButton
        :label="'削除'"
        :type="'button'"
        color="'primary'"
        :outlined="false"
      />
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
      <div class="buttons">
        <BaseIconButton
          :label="'言語を追加'"
          :type="'button'"
          :color="'primary'"
          :outlined="false"
        />
        <BaseButton :label="'送信'" :type="'submit'" :color="'primary'" />
      </div>
    </form>
  </div>
</template>

<style scoped>
.other-language-wrapper {
  display: flex;
  height: auto;
}

.other-language-form {
  width: 800px;
  border: 1px solid;
}

.buttons {
  display: flex;
}
</style>
