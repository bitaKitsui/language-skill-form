<script setup lang="ts">
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import { LANGUAGE_SELECTS, LANGUAGE_LEVEL_SELECTS } from '../../constants'
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div class="wrapper">
    <BaseTitle :value="'語学力（その他言語）'" />
    <form>
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
      /><BaseSelect
        :id="'level'"
        :label="'レベル'"
        :name="'select-level'"
        :options="LANGUAGE_LEVEL_SELECTS"
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
.wrapper {
  display: flex;
}

.buttons {
  display: flex;
}
</style>
