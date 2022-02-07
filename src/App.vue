<script setup lang="ts">
import './styles/reset.css'
import BaseButton from './components/atoms/BaseButton.vue'
import BaseModal from './components/organisms/BaseModal.vue'
</script>

<template>
  <div>
    <BaseButton
      :label="'Open Modal'"
      :type="'button'"
      :color="'secondary'"
      :outlined="true"
    />
    <BaseModal />
  </div>
</template>

<style></style>
