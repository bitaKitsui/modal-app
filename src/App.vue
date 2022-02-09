<script setup lang="ts">
import { ref } from 'vue'
import './styles/reset.css'
import BaseModal from './components/organisms/BaseModal.vue'
import BaseOpenButton from './components/atoms/BaseOpenButton.vue'

const isActive = ref(false)

const handleOpen = () => {
  isActive.value = true
}

const handleClose = () => {
  isActive.value = false
}
</script>

<template>
  <div class="column">
    <BaseOpenButton
      :label="'Open Modal'"
      :type="'button'"
      :width="'140px'"
      @open="handleOpen"
    />
    <BaseModal :is-active="isActive" @close="handleClose" />
  </div>
</template>

<style>
.column {
  margin-top: 40px;
  display: flex;
  justify-content: center;
}
</style>
