<script setup lang="ts">
import LanguageSkillForm from './components/templates/LanguageSkillForm.vue'
import './styles/reset.css'
</script>

<template>
  <LanguageSkillForm />
</template>

<style>
#app {
  width: 100vw;
  height: 100vh;
  font-size: 16px;
}

input {
  border: 1px solid;
  border-radius: 5px;
  height: 30px;
}

select {
  width: 100%;
  height: 30px;
  appearance: none;
  background: none;
  border: none;
  line-height: 30px;
}

button {
  border: 1px solid;
}
</style>
