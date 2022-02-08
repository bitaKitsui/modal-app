<script setup lang="ts">
import BaseBody from '../molecules/BaseBody.vue'
import BaseFooter from '../molecules/BaseFooter.vue'
import BaseHeader from '../molecules/BaseHeader.vue'
</script>

<template>
  <div class="modal">
    <BaseHeader />
    <BaseBody />
    <BaseFooter />
  </div>
</template>

<style scoped>
.modal {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border: 1px solid;
  border-radius: 4px;
  min-height: 300px;
}
</style>
