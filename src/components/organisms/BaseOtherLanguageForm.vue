<script setup lang="ts">
import { toRefs } from 'vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseIconButton from '../atoms/BaseIconButton.vue'
import BaseSelect from '../atoms/BaseSelect.vue'
import BaseButton from '../atoms/BaseButton.vue'
import { LANGUAGE_SELECTS, LANGUAGE_LEVEL_SELECTS } from '../../constants'

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
        <div class="form-selects">
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
        </div>
      </div>
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
  border: 1px solid;
}

.form-header {
  width: 100%;
  height: 40px;
  background: #769dbb;
  display: flex;
  justify-content: flex-end;
}

.form-selects {
  padding: 20px;
}

.buttons {
  display: flex;
}
</style>
