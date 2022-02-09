<script setup lang="ts">
import './styles/reset.css'
import BaseModal from './components/organisms/BaseModal.vue'
import BaseOpenButton from './components/atoms/BaseOpenButton.vue'
</script>

<template>
  <div class="column">
    <BaseOpenButton :label="'Open Modal'" :type="'button'" :width="'140px'" />
    <BaseModal />
  </div>
</template>

<style>
#app {
  display: flex;
  justify-content: center;
}

.column {
  width: 400px;
  margin-top: 40px;
}
</style>
