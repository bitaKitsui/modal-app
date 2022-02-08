<script setup lang="ts">
import './styles/reset.css'
import BaseButton from './components/atoms/BaseButton.vue'
import BaseModal from './components/organisms/BaseModal.vue'
</script>

<template>
  <div class="column">
    <BaseButton
      :label="'Open Modal'"
      :type="'button'"
      :color="'secondary'"
      :outlined="true"
    />
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

button {
  border: 1px solid;
  border-radius: 4px;
}
</style>
