<script setup lang="ts">
import { ref } from 'vue'
import BaseBody from '../molecules/BaseBody.vue'
import BaseFooter from '../molecules/BaseFooter.vue'
import BaseHeader from '../molecules/BaseHeader.vue'
import { MODAL_BODY } from '../../constants'

const isActive = ref(false)
</script>

<template>
  <div v-if="isActive" class="modal">
    <BaseHeader :header-title="'Modal Title'" />
    <BaseBody :body="MODAL_BODY" />
    <BaseFooter />
  </div>
</template>

<style scoped>
.modal {
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border: 1px solid;
  border-radius: 4px;
  min-height: 300px;
}
</style>
