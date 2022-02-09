<script setup lang="ts">
import BaseCloseButton from '../atoms/BaseCloseButton.vue'
import BaseFunctionButton from '../atoms/BaseFunctionButton.vue'

interface Emits {
  (event: 'close'): void
}

const emit = defineEmits<Emits>()

const handleClick = () => {
  emit('close')
}
</script>

<template>
  <div class="footer">
    <BaseCloseButton
      :label="'Close'"
      :type="'button'"
      :color="'primary'"
      :outlined="true"
      :width="'70px'"
      @close="handleClick"
    />
    <BaseFunctionButton
      :label="'Secondary Action'"
      :type="'button'"
      :outlined="false"
      :width="'170px'"
    />
  </div>
</template>

<style scoped>
.footer {
  display: flex;
  justify-content: flex-end;
}
</style>
